---
title:  "Assessing Crowd Behaviour w/ LLM - BBC  Africa Eye - Kenya Anti-tax Protesters"
mathjax: true
layout: post
categories: LLM-as-a-Judge, LLM experiment, Crowd Behavior 
---

What insights might an LLM offer if tasked with objectively observing the events presented  in <a href="https://www.bbc.com/news/articles/c8jexr9yv0do" target="_blank"> the recent BBC video</a>? 

<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/mistral-5mins-overall-scores.png?raw=true' width='450' height="400" style="width: 500px !important; height: 300px !important;"> 
</p> 
<p align='center'>Figure 1: General attitudes in the video </p>


This post is basically me playing around with the idea of using a Large Language Model to see if it can offer an objective, almost 'just the facts' kind of take on what went down. We'll use the video as our guinea pig to explore what these AI tools can and can't really tell us about human behavior and how crowds act in situations like this. Heads up: this isn't about saying what's right or wrong, just a bit of a techie thought experiment! 


Now, watching that BBC video myself, a few things popped into my head about how the story was being told. You know, sometimes when you watch something, you can't help but feel like the person showing it to you has a certain angle they're leaning towards. There were moments where I thought, "Hmm, is that really what happened?" Like in one scene, the camera's behind a group of people, so everyone's facing away, but the commentary made it sound like one person specifically chose to turn their back to the camera. Or the bit about the same individual putting on a mask right before things got serious – well, they weren't the only one with a mask, and it wasn't exactly clear when they put it on. Little things like that made me wonder about how objective the whole thing was, almost like in some episode of Black Mirror, you know?

Then there's the crowd dynamics. Despite the warning shots and tear gas, they kept advancing. I suppose democracy and civic literacy could be lauded for that. All the same, it makes you think about how crowd control tactics, which maybe worked differently before, don't seem to have the same impact anymore, at least not in this case. Or maybe, like some people are saying, the energy and drive of the crowd were just amplified by growing frustration with the authorities. 

Irrespective, could an LLM watch this same video and give us a truly unbiased read on what's happening with the people and the crowd? Could it cut through the storytelling and just look at the raw actions and reactions? That's what I'm curious to explore.



## The Setup

- **The input** to the LLM is the transcript from the video. In addition to having the entire transcript as a single block of text, the transcript is sectioned into eight 5-minutes and four 10-minutes contiguous segments. That makes for a total of 13 records. 

- **The models** used in this exercise are [Qwen 32B](https://huggingface.co/Qwen/QwQ-32B) and [Mistral-Small-3.1 24B](https://huggingface.co/mistralai/Mistral-Small-3.1-24B-Instruct-2503). Qwen loves to overthink! I fear that my laptop was not the best setup for it, sadly.  

- **Evaluation metrics** are described based on current thinking about crowd dynamics. For instance, considering the proportionality of authority response or the role of both sides in escalation and de-escalation of issues. Look, I'm no expert on this and I'm just piecing this together from what I've been reading – definitely not the final word on it. The 14 metrics detailed in this post are described at the end of this post. This list is by no means exhaustive.   

On top of looking at how the LLMs analyze the crowd behavior, I also threw in a few extra checks to see how reliable the LLMs themselves are being. The LLM in this setup is pretty much an LLM-as-a-Judge. 

- **Experiment runs:** Qwen takes a lot of time and resources to run. As this was intended to be a light experiment, I only ran one iteration with it. Mistral 24B, on the other hand, is much faster, so I ran 3 evaluation rounds with it. 

- **Analysis:** The analysis presented next is primarily descriptive. 

- **Limitations:** Only the video's transcript is used as input. 




## Some results
 **LLM Suitability:** Table 1 below shows how well the LLMs worked with the provided input and whether they seemed to lean towards a particular score in the provided binary and likert scales. The runs with data points from the 5-minutes long segments and using Mistral LLM seem to be relatively consistent across the different checks. The next sections will focus on that set of results. 

 <p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/01-LLM-cred-check.png?raw=true' width='450'> 
</p> 
<p align='center'>Table 1: Checking LLM's suitability for the task</p>

 
 
 **What can be said of the role of the different parties?** 
 Figure 1 presents the LLM scores on the general attitude towards the demonstrators compared to that towards the authorities. On the graph, the metric score is on the primary y axis, represented by the bars. The metric score is a value between 0 and 1 (percent value in decimal format). On the secondary y axis (the line snaking across the graph) is the model's confidence in the score it assigned. This too is a percent value. These values are averages of the scores assigned by the model to the entire sample of 5-minutes segments, and where the model felt (:)) that it had enough infor to make a call. 
 
 - Sometimes, the model considered the text not to have enough information for it to infer, and therefore, it returned -99 for `I don't know`.

 - A metric score of 1 means: 1 = 100% = Yes
 
 - A metric score of 0 means: 0 = 0% = No
 
 
<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/mistral-5mins-overall-scores.png?raw=true' width='550' height="400" style="width: 500px !important; height: 300px !important;"> 
</p> 
<p align='center'>Figure 1: General attitutes in the video </p>

 A couple of observations: 
 - It looks like the way the report talks about the authority figures isn't quite the same as how it portrays the demonstrators. If you look at Figure 1, the overall feeling towards the authorities is not found to be similar to that towards the demonstrators.
 - In addition, the report does not seem to sufficiently present the position of both sides (demonstrators and authorities).  


 Figure 2 shows the models' take on how the demonstrators and the enforcers acted, specifically looking at whether they seemed to be helping calm things down or not. You can read this chart just like the last one we looked at (Figure 1).
 
 <p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/mistral-5mins-crowd-mind-scores.png?raw=true' width='550' height="400" style="width: 500px !important; height: 300px !important;"> 
</p> 
<p align='center'>Figure 2: Demonstrators Vs Enforcers behaviour</p>

 

There's definitely a lot to unpack in this chart, but I'll leave my own interpretation out of it for now. Looking at this, though, it seems like the LLM is suggesting that both the demonstrators and the enforcers had a role to play in how things unfolded.
 


## Closing thoughts
This was an interesting exercise. The value we derive from an LLM's analysis is heavily contingent on the clarity and nuance of our own understanding of the subject matter. In this case, having a foundational grasp of crowd dynamics – even a rudimentary one gleaned from current literature – proved crucial in formulating the evaluation metrics. Without that initial framework, instructing the model to identify proportionality of response or contributions to de-escalation would have been akin to asking it to find something without describing what "something" looks like.

Therefore, the process becomes a collaborative one. We bring our human understanding, our contextual awareness, and our formulated questions. The LLM then processes the information, identifies patterns, and offers insights based on its training data. However, the interpretation of those insights, their significance, and their alignment with real-world understanding remain firmly in our hands. 



## Metrics 
 
 <p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/tbl-metrics-overall.png?raw=true' width='450'> 
</p> 
<p align='center'>Table 2: Metrics on general attitude</p>


 <p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/bbc-video/tbl-metrics-crowd-mind.png?raw=true' width='450'> 
</p> 
<p align='center'>Table 3: Metrics on some crowd dynamics</p>

