---
title:  "What is Hypergraph Learning?"
mathjax: true
layout: post
categories: graph learning, hypergraph, convolution  
---


<p align='center'><b> Constructing your own hypergraph</b><br\>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/hgnn_construction.png?raw=true' width='450'>
</p> 


**TLDR;**
- Real-world scenarios entail complex relationships between multiple entities. 
- Hypergraphs capture more than pairwise relationships, encoding complex relationships. 
- You can construrct a hypergraph for non-graphical data; define your nodes and hyperedges using various similarity-based approaches. 


**Beyond Pairs: Exploring the Power of Graph Learning and Hypergraphs**

Many real-world scenarios involve complex relationships that might not sufficiently represented by pair-wise associations. Graph learning offers a powerful framework to understand and leverage the interconnectedness of data. 

Graphs are a way to both store and encode relationships. They allow us to move beyond individual data points and consider the intricate web of connections that define a system. A graph consists of:

- Vertices (or nodes): These represent entities or objects. In the context of images, a vertex could be a pixel, a region of interest, or even an entire image.

- Edges (or links): These define the relationships or connections between pairs of vertices. An edge might represent the spatial proximity of pixels, the similarity between images, or interactions between proteins.


**Learning with Hypergraphs**
Graph learning tasks are diverse, including classifying individual nodes, predicting links between nodes, grouping similar nodes, or even understanding the structure of entire graphs. Many deep learning models on graphs ultimately learn node representations (embeddings) by considering the graph's structure and the features of connected nodes.

*Stepping Beyond Pairwise Connections:* While graphs effectively model pairwise relationships, many systems exhibit dependencies that involve more than just two entities simultaneously. Imagine a research collaboration involving multiple scientists, or a biological pathway where several proteins interact at once. Standard graphs fall short in capturing these higher-order correlations. This is where hypergraphs come into play.


*A hypergraph* is a generalization of a traditional graph where an edge (now called a hyperedge) can connect two or more vertices. This allows for a much richer representation of complex associations. Think of a hyperedge as a group of related entities, capturing the idea that their interaction is not just a series of pairwise relationships, but a collective one.

<p align='center'><b> Formal representation of a hypergraph</b><br\>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/hgnn_intro.png?raw=true' width='450'>
</p> 

Hypergraphs are often represented using an incidence matrix, where rows correspond to vertices and columns represent hyperedges. An entry in the matrix indicates whether a particular vertex belongs to a specific hyperedge. This is demonstrated in the figure above. 


*Hypergraph Estimation:* Since data isn't always naturally structured as a hypergraph, various hypergraph estimation methods exist to infer these higher-order relationships from data. These methods can be based on the similarity between entities (e.g., k-nearest neighbors, k-means clustering), attributes of the entities, or even hop-aggregates in an existing graph. This is illustrated in the very first figure above. From this estimation exercise, the hypergraph incidence matrix is constructed. 


*Formal Definition:* Formally, a hypergraph `$𝐺 = (𝑉 ,𝐸,𝐻,𝑊 ,𝑋)$` consists of a set of  vertices `$𝑉 = {𝑣1,…,𝑣𝑛}$` and a set of hyperedges `$𝐸 = {𝑒1,…,𝑒𝑚}$` depicting the relationships between the vertices. The associated incidence matrix `$𝐻 ∈ ℝ𝑛×𝑚$` and hyperedge weights `$𝑊 ∈ ℝ𝑚×𝑚$` encode relational structure, while the vertex features `$𝑋 ∈ ℝ𝑛×𝑑$` capture content information. The incidence matrix `$𝐻$` is a binary matrix and the strengths of the hyperedge connections are represented in the diagonal matrix `$𝑊$`. The feature matrix `$𝑋$` holds the input features of each vertex as a one-dimensional vector `$𝑋(𝑣𝑖) = 𝑥𝑖 ∈ ℝ𝑑$`.

<p align='center'> 
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/hgnn-math-defn.png?raw=true' width='450'>
</p> 


*Laplacian of a Hypergraph:* The Laplacian of graphs is a critical operator in graph signal processing and forms the basis of most graph neural networks taking on different normalization forms in some models and being an important research topic for enhancing the prediction and  computational performance of deep learning models for graph data. It is a critical component of learning with graphs. Will delve into it in the next post. 

