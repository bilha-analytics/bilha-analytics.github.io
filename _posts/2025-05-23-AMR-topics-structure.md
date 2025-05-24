---
title:  "Exploring Research Priorities for Community-level AMR Tools"
mathjax: true
layout: post
categories: AMR, antimicrobial resistance, topic analysis, topic modeling, NLP
---



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 1: Topics across the entire dataset</p>



Antimicrobial resistance (AMR) is a global public health challenge. It refers to the alarming ability of microorganisms like bacteria, viruses, fungi, and parasites to resist antimicrobial drugs. This makes infections way tougher to treat, and escalates the risks of disease spread, severe illness, and even death. While these microorganisms naturally evolve, our actions, especially using too many antibiotics or using them incorrectly, have sped up the development and proliferation of this concerning process. 

How we use antimicrobials at home (for ourselves and for animal care/husbandry) and at local pharmacies and health facilities contributes to AMR. Think about things like how we prescribe or purchase antibiotics, how well we adhere to dosage instructions, our practices around infection prevention, and even environmental factors such as access to clean water and proper sanitation. These community-level dynamics really show us how our collective habits drive the spread of resistance.  


Then, COVID-19 happened, and it threw a whole new wrench into the AMR picture. The pandemic brought a complex mix of impacts for AMR. On one hand, there was increased use of broad-spectrum antibiotics in hospitals, which potentially gave the microorganisms more opportunities to evolve and spread resistant strains. For instance, studies from Qatar and Egypt report increased spread in resistant bacteria during the pandemic, while a study from Tanzania finds that antibiotic consumption soared, with specific drugs like levofloxacin, azithromycin and cefotaxime seeing significant spikes. Conversely, the pandemic also pushed us to improve infection prevention and control practices, and some regions reported a decrease in community antibiotic consumption (see references below for more and why). One example here is in Italy, where they observed a decrease in community antibiotic use during the pandemic.   


Given these multifaceted impacts, one may wonder how research priorities and discourse around AMR have shifted, if at all. 



# What we investigated and how
This piece is a curious investigation into the kind of community-related AMR research that was happening before the pandemic versus after the pandemic. Now, there are several aspects we could consider when exploring community-level AMR. For instance,

- Behavioural aspects: why people misuse antibiotics, public awareness, cultural factors.

- Social determinants: how poverty, education, access to healthcare influence AMR.

- Surveillance: monitoring resistance patterns in the community. 

- Interventions: community-based programs to reduce antibiotic use or improve hygiene.

- Environmental links: AMR in water, soil, agriculture, and its impact on human communities. 

- Policy and stewardship: community-level antibiotic stewardship programs, local guidelines. 

**A multi-tech lens:** That's a lot to cover! Therefore, this time around, we take a techie's lens - and by that, we mean focusing on any tools and techniques, cutting across both computational and biomedical domains. This narrows our focus to exploring tools and techniques (regardless of other factors, such as whether the tools are for surveillance or identifying social determinants) that might suggest readily actionable areas. A detailed description of the PubMed search term is provided towards the end of the article. 



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
Let's first dive into the prominent topics across the dataset and then a closer look at the key research priorities that dominated before versus after and during COVID-19. 

## Topics across the entire research period

Figure 1 below depicts the main topics discovered. The color-coded regions are document clusters for a given topic. The larger the region the more documents fall under that topic. To complement this figure, figure 2 lists out the top 10 terms for the first 4 popular topics. The 4 popular topics are

- Urinary Tract Infections (UTIs) and infections in nursing homes. 

- Antibiotic prescription practices. 

- Pneumonia or upper respiratory tract infections. Notice how the top terms in this topic include children and hospitalization. 

- Bacteria or Methicillin-resistant Staphylococcus Aureus (MRSA) aspects that may concern understanding the mechanisms of resistance and exploring new treatment and prevention strategies.  



<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 1: Topics across the entire dataset.</p>
<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/topic-words-all.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 2: Top 10 terms for the 4 popular topics.</p>




## Before Vs During and after pandemic
Figure 3 is a distribution of the above identified topics by pandemic period. 

  - The focus before pandemic was on  UTI and nursing homes, pneumonia and upper respiratory tract infections, and antibiotic prescription practices. 

  - During and after the pandemic, there's a shift that prioritizes antibiotic prescription practices, followed by UTIs and nursing homes, and then pneumonia. 


<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/topics-by-covid-period-from-all-data-fit.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 3: Topic clusters before pandemic.</p>



Similar to figures 1 above, figure 4 shows the main topics before the pandemic, while figure 5 illustrates the main topics during and after pandemic. 


- Before the pandemic, pneumonia and bacterial strains are top two, followed by antibiotic prescription practices and UTI and elderly care. 

<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters__Before COVID-19.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 4: Topic clusters before pandemic.</p>


- During and after the pandemic, focus is primarily on AMR as a general topic, and then specifically about SARS-COV2 related vaccine research. 

<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/document-clusters__During or After COVID-19.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 5: Topic clusters during and after pandemic.</p>


 A deep dive into documents published during and after the pandemic is presented in figures 6 and 7. 

- The main disease and condition areas remain consistently important. Our thematic map (figure 7) confirms sustained focus on Urinary Tract Infections (UTI), pneumonia, upper respiratory tract infections, challenges in nursing homes/elderly care, and the persistent threat of MRSA/bacterial strains and their resistance. 

- In addition to these core areas, emerging (or declining) areas suggest a broader focus on global public health goals, potentially aligning with guidance from the WHO. 

- Furthermore, potential niche areas seem to particularly concern patients requiring complex medical care. 

  - Parenteral Nutrition (PN) and Central Venous Catheters (CVCs) are methods for directly delivering nutrients and medication to patients, and that present a high risk for catheter-related bloodstream infections (CRBSI). Due to their invasive nature, patients relying on PN and CVCs are often on prolonged courses of antimicrobials to manage or prevent infections. This extended exposure significantly contributes to the development of antimicrobial resistance, making CRBSIs caused by resistant bacteria especially challenging to treat. AMR studies in this niche area are crucial for identifying strategies to prevent infections (e.g., through improved catheter care or antimicrobial-impregnated catheters) and for investigating novel antimicrobial approaches to combat resistant infections in these vulnerable patient populations.




<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/thematic-map-1-abs-3gram.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 6: Thematic map of 3-gram terms in abstracts published during or after pandemic.</p>


<p align='center'>
    <img src='https://github.com/bilha-analytics/bilha-analytics.github.io/blob/master/res/amrt1/after-covid-abs.png?raw=true' width='1350' style="width: 95% !important;"> 
</p> 
<p align='center'>Figure 7: Summary of abstract text during and after pandemic.</p>


# Concluding remarks
Our exploration into community-level antimicrobial resistance (AMR) research, viewed through a multi-tech lens, reveals that the landscape is dominated by four enduring areas: Urinary Tract Infections (UTIs) and infections in nursing homes, the critical domain of antibiotic prescription practices, the persistent challenge of pneumonia and upper respiratory tract infections, and bacteria and MRSA research.

The comparison between the pre-pandemic era and the period during and after COVID-19 shows a clear shift in focus. Before the pandemic, research prominently addressed UTIs and nursing homes, pneumonia and upper respiratory tract infections, and antibiotic prescription practices. While during and after the pandemic, we observe a noticeable re-prioritization: antibiotic prescription practices have moved to the forefront, and there is a broader emphasis on global public health goals, and bacterial or vaccine research. 


For our techies, where do we go from here? Our insights highlight potential junctures for innovation. For instance, imagine building more sophisticated AI models to predict AMR outbreaks in nursing homes, designing smarter decision-support tools for antibiotic prescription, or creating integrated data platforms that track global AMR trends. Or imagine novel antimicrobial strategies for resistant pathogens like MRSA, and augmenting invasive therapeutics to reduce risk of bloodstream infections and bacterial biofilms. What do you think?   


 



# Other Notes/Context 
- Our search strategy on PubMed was intended to capture a broad yet relevant collection of research on community-level AMR tools. The search term used was 

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

