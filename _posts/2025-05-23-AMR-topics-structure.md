---
title:  "WIP: AMR Topic Shifts Before & After COVID-19 - Tools and Techniques for Community-level AMR"
mathjax: true
layout: post
categories: AMR, antimicrobial resistance, topic analysis
---



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 1: Topics across the entire dataset</p>



Antimicrobial resistance (AMR) is a global public health challenge. It refers to the alarming ability of microorganisms like bacteria, viruses, fungi, and parasites to resist antimicrobial drugs. This makes infections way tougher to treat, and escalates the risks of disease spread, severe illness, and even death. While these microorganisms naturally evolve, our actions, especially using too many antibiotics or using them incorrectly, have sped up the development and proliferation of this concerning process. 

How we use antimicrobials at home (for ourselves and for animal care/husbandry) and at local pharmacies and health facilities contributes to AMR. Think about things like how we prescribe or purchase antibiotics, how well we adhere to dosage instructions, our practices around infection prevention, and even environmental factors such as access to clean water and proper sanitation. These community-level dynamics really show us how our collective habits drive the spread of resistance.  


Then, COVID-19 happened, and it threw a whole new wrench into the AMR picture. The pandemic brought a complex mix of impacts for AMR. On one hand, there was increased use of broad-spectrum antibiotics in hospitals, which potentially gave the microorganisms more opportunities to evolve and spread resistant strains. For instance, studies from Qatar and Egypt report increased spread in resistant bacteria during the pandemic, while a study from Tanzania finds that antibiotic consumption soared, with specific drugs like levofloxacin, azithromycin and cefotaxime seeing significant spikes. Conversely, the pandemic also pushed us to improve infection prevention and control practices, and some regions reported a decrease in community antibiotic consumption (see references below for more and why). One example here is in Italy, where they observed a decrease in community antibiotic use during the pandemic.   


Given these multifaceted impacts, one may wonder how research priorities and discourse around AMR have shifted. This article takes a look at the topics in published research abstracts from before and after the COVID-19 pandemic.


# What we investigated and how
This piece is a curious investigation into the kind of community-related AMR research that was happeninig before the pandemic versus after the pandemic. Now, there are several aspects we could consider when exploring community-level AMR. For instance,

- Behavioural aspects: why people misuse antibiotics, public awareness, cultural factors.

- Social determinants: how poverty, education, access to healthcare influence AMR.

- Surveillane: monitoring resistance patterns in the community. 

- Interventions: community-based programs to reduce antibiotic use or improve hygiene.

- Enviromental links: AMR in water, soil, agriculture, and its impact on human communities. 

- Policy and stewardship: community-level antibiotic stewardship programs, local guidelines. 

**A multi-tech lens:** That's a lot to cover! Therefore, this time around, we take a techie's lens - and by that, we mean focusing on any tools and techniques, cutting across both computational and biomedical domains. This narrows our focus to exploring tools and techniques (regardless of other factors, such as whether the tools are for surveillance or identifying social determinants) that might suggest actionable areas. A detailed descrition of the PubMed search term is provided towards the end of the article. 



To do this we mine and analyze a collection of 880 abstracts from PubMed (a vast repository of biomedical literature). Table 1 below describes the data used for this analysis. Of the 880 documents, a striking 41% were published during or after the pandemic. To put that into perspective: just five years of post-COVID research accounts for almost half of our dataset, while the remaining documents span over five decades of research prior to the pandemic. This rapid increase in publication volume, might hint at a significant acceleration in AMR research activity coinciding with the global health crisis. 


<caption>Table 1: The number of documents</caption>
<table>
  <thead>
    <tr>
      <th>period</th>
      <th>count</th>
      <th>proportion</th>
      <th>min_year</th>
      <th>max_year</th>
      <th>n_years</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Before COVID-19</td>
      <td style="text-align:right;">519</td>
      <td style="text-align:right;">59%</td>
      <td style="text-align:right;">1967</td>
      <td style="text-align:right;">2019</td>
      <td style="text-align:right;">52</td>
    </tr>
    <tr>
      <td>During or After COVID-19</td>
      <td style="text-align:right;">361</td>
      <td style="text-align:right;">41%</td>
      <td style="text-align:right;">2020</td>
      <td style="text-align:right;">2025</td>
      <td style="text-align:right;">5</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Total</td>
      <td style="text-align:right;">880</td>
      <td style="text-align:right;">100%</td>
      <td colspan="3"></td>
    </tr>
  </tfoot>
</table>




Of course, it is important to remember that this analysis is a descriptive review, essentially looking for patterns and trends in the available research abstracts, but in no means offering a causal explanation or a comprehensive systematic review. It is an insightful snapshot of how research attention has shifted.  


# Observations
Let's dive into the prominet topics across the dataset and then a closer look at the key research priorities that dominated before versus after and during COVID-19. 

## Topics across the entire research period

Figure 1 below depicts the main topics spanning the entire reserch period. The color-coded regions are document clusters for a given topic. The larger the region the more documents fall under that topic. To complement this figure, figure 2 lists out the top 10 terms for the top 4 topics in this dataset. The top 4 topics are

- Urinary Traact Infections (UTIs) and infections in nursing homes. This is titled `Topic 0` in the figure 2. 

- Antibiotic prescription practices. This is titled `Topic 1` in the figure 2. 

- Pneumonia or upper respiratory tract infections. This is titled `Topic 2` in the figure 2. Notice how the top terms in this topic include children and hospitalization. 

- Methicillin-resistant Staphylococuss Aureus (MRSA) aspects. This is titled `Topic 3` in the figure 2. 



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 1: Topics across the entire dataset.</p>
<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/topic-words-all.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 2: Top 10 terms for the top 4 topics.</p>




## Before Vs During and after pandemic
Similar to figures 1 and 2 above, figures 4 and 5 show the main topics before the pandemic, while figures 6 and 7 illustrate the main topics during and after pandemic. 


<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters__Before COVID-19.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 4: Topic clusters before pandemic.</p>
<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/topic-words-b4-covid.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 5: Top 10 terms for the top 4 topics before pandemic.</p>



- Before the pandemic, pneumonia and bacterial strains are top two, followed by antibiotic prescription practices and UTI and elderly care. 



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters__During or After COVID-19.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 6: Topic clusters during and after pandemic.</p>
<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/topic-words-a5-covid.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 7: Top 10 terms for the top 4 topics during and after pandemic.</p>


- During and after the pandemic, focus is primarily on AMR as a general topic, and potentially regarding hospital-acquired infections, and nursing homes and elderly care. 

    - A deep dive into these documents is presented in figures 8 and 9. 

    - In the thematic map (figure 7), the main disease/condition areas remain. I.E. UTI, pneumonia and upper respiratory tract infections, nursing homes/elderly care, and MRSA/bacterial strains and resistance. 
    
    - In addition, emerging (or declining) areas suggest a focus on global public health goals, potential as per WHO guidance. TODO: more info here
    
    - From this, it is not quite clear what specific aspects of AMR, aside from SARS-COV2 related vaccine research, and the second main topic during the period, are being investigated. Unfortunately, with the time available for this analysis, exploring that would be an exercise for another day. 

    - What do you think is happening here? 



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/thematic-map-1-abs-3gram.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 8: Thematic map of 3-gram terms in abstracts published during or after pandemic.</p>


<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/after-covid-abs.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 9: Summary of abstract text during and after pandemic.</p>


 



# Other Notes/Context 
- Our search strategy on PubMed was intended to capture a broad yet relevant collection of community-level AMR research as **pertains to what actions....**. The search term used was 
```("Anti-Microbial" or "antimicrobial" or "anti-biotic" or "antibiotic") and (resistance) and (“community level” or “community-level” or “market side” or “demand side” or  “at-home“  or “at home” ) and (tools or methods or techniques or models or "deep learning" or "machine learning" or "generative AI" or "AI" or "LLM" or "large language models")```





# References 
- [WHO AMR page](https://www.who.int/health-topics/antimicrobial-resistance) 

- [WHO global research priorities for antimicrobial resistance in human health](https://doi.org/10.1016/S2666-5247(24)00134-4)

- [Antimicrobial resistance burden pre and post-COVID-19 pandemic with mapping the multidrug resistance in Egypt: a comparative cross-sectional study](https://doi.org/10.1038/s41598-024-56254-4)

- [Antibiotic Utilisation Patterns in Tanzania: A Retrospective Longitudinal Study Comparing Pre- and Post-COVID-19 Pandemic Using Tanzania Medicines and Medical Devices Authority Data](https://doi.org/10.1101/2023.11.27.23299060)

- [Antimicrobial Resistance in Qatar: Prevalence and Trends Before and Amidst the COVID-19 Pandemic](https://doi.org/10.3390/antibiotics13030203)

- [Impact of the COVID-19 pandemic on community antibiotic consumption in the EU/European Economic Area: a changepoint analysis](https://doi.org/10.1093/jac/dkad273)

- [An Improvement in the Antimicrobial Resistance Patterns of Urinary Isolates in the Out-Of-Hospital Setting following Decreased Community Use of Antibiotics during the COVID-19 Pandemic](https://doi.org/10.3390/antibiotics12010126)

- In addition to our own data mining and analysis tools, we also made use of  
    - [BibliometriX, an R tool for science mapping](https://www.bibliometrix.org/)
    - [BERTopic, a topic modelling tool with various NLP and LLM techniques](https://maartengr.github.io/BERTopic/index.html)

- 

