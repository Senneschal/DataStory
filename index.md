---
feature_text: |
    # <span style="color:#333333">Globalized Analysis of Medical Data </span> 
feature_image: "./assets/world.png"
background-color: #333333
---

__All over the world, lots of data is gathered concerning people's health. Can we extract useful information from this data to improve the quality of life of societies? In this project, we specifically want to get to know which diseases have the biggest negative impact on societies' quality of life, and what factors influence this.__

For this analysis, data from the Global Burden of Diseases [dataset](http://ghdx.healthdata.org/gbd-results-tool) was used.

##### Measures

Which diseases have the most significant negative impact on society's quality of life? How does this differ between countries and how does it change over time? <br>

To answer this question, we first need to decide how we quantify the impact a disease has on quality of life of a society. The easiest way to look at this, is to look at the number of deaths a disease causes: after all, you can't have any "quality of life" anymore if your life has come to an end. <br>

So, let's start off by looking at which diseases caused the most deaths worldwide, in every year since 1990.

{% include Amount_of_recorded_deaths.html %}

We find that cardiovascular disease and cancer are globally by far the most common causes of death, followed at a distance by cancers, with all other causes following at more of a distance behind cancer. <br>

However, the causes of death strongly vary between different countries. <br>
The following map visualizes the mortality of different diseases for each country. The disease can conviently be chosen by using the drop down menu.

{% include 1.1.2.html %}

When looking at cardiovascular disease, we see that it has become increasingly prevelent in developing countries while its prevelence is decreasing in developed countries. Note that Syria is a clear outlier in the Middle East, this may very well be a result of war.

The Global Burden of Diseases dataset also contains a number of other interesting measures to see the impact of diseases on people's quality of life.

{% include comp_of_measures.html %}

##### Clustering

To compare how diseases develop in different countries, we took disease data from The Global Burden of Diseases dataset for each country and disease, and investigated which countries are correlated. There is several ways in which a disease can be strongly correlated between countries. Neighbouring countries may be strongly correlated because the disease could spread accross the borders. But also countries that are far apart from each other could be highly correlated as a result of frequent air travel between them. Another way distant countries could strongly correlated is because of past colonization, which may cause the populations to have similar genetics that makes them vulnerable to a specific disease, etc. We then grouped the countries for specific diseases such that in each groups are correlated with each other above a certain threshold value. 

The slider beneath the plots determines the "coarseness" of the grouping. It gives the average lack of positive correlation allowed within groups: a value of ***0*** means perfect correlation, ***1*** on average no correlation within group and values greater than one include even negatively correlated countries in the group. Thus if the slider is all the way to the right, almost every country is concidered to be in the same group while if the slides is moves all the way to the left, almost every country is concidered to be its own group.

{% include cluster1.html %}

This plot shows strong difference between the Western and Eastern world, especially in Europe. The border between groups defintely differentiates between what is commonly known as Western and Eastern Europe. Interestingly, we saw in the previous part that deaths of cardiovascular diseases are decreasing in the developed world and increasing in the developing one.
But looking at correlation of DALYs, much of the developed and developing world is grouped in the same group, implying similar development. This implies that while deaths from these diseases are decreasing in developed countries, people still live with them and suffer from them.

In general, the groups do not appear to be confined to geographical groupings. This supports the hypothesis that cardiovascular diseases may depend mainly on societal and economic factors.

{% include cluster2.html %}

For respiratory and tuberculosis, the correlation appears stronger, as larger groups form at lower grouping tresholds. The grouping also appears more dependent on geography as neighbouring countries quickly form groups, which strongly differs from the societal and economic factors that showed to govern cardiovascular disease. This makes sense, as this is now an infectious disease we are looking at, which can truly spread accros countries.

An interesting correlation that shows up is the strong correlation between Germany and Argentina. This could just be a coincidence, but there are strong historical ties between the countries and a lot of German expats/people with German roots living in Argentina ([learn more](https://en.wikipedia.org/wiki/German_Argentine)). People may transfer the diseases from country to country when visiting relatives. We are also looking at a long term measure such as DALY's. One hypohesis that could be made is that German Argentines with dual citizenship might seek treatment in Germany, a country ranked higher in healthcare comparisons. However, more research would be needed to comfirm these speculations.

{% include cluster3.html %}

For infectious diseases, Incidence might be a better measure. Indeed, looking at Incidence as opposed to DALYs shows some fascinating things: the correlations are strong, indicating an infectious disease. At coarse grouping, the entire world except for a select few countries are positively correlated, while these countries actually appear quite negatively correlated to the bigger group. The interesting observation that can be made is that all these countries in their own separate groups are countries that have been subject to considerable instability, strife and even civil war in the time period considered. (Liberia, Chad, Afghanistan...) This may indicate that the disease incidence in conflict prone countries is simialr between these countries and very different and not positively correlated with the rest of the world. In essence, these countries may be "isolated", and not part of a global network of disease transmission. However, due to strife and instability, the medical data from these countries might just be incomplete or faulty.

Note that, the old adage "correlation does not imply causation" is very much applicable to these findings. That two countries are correlated only means that the development of the disease in the countries is similar. The reasons for this similarity may be many: direct spread of disease, geographical factors, social, economic factors and more. These reasons and risk factors for disease will be explored in the next sections. 

##### Economical and political factors

We saw in the first section that some causes of death were more significant than others. 
If we add the life expectancy and the GDP per capita, we notice that the suggestions we made previously are realistic. <br>
Indeed, we notice that cardiovascular diseases and apply precipitously to the most developed countries and to the richest countries while other causes of death apply more to the least developed countries. <br>
Cardiovascular diseases, Musculoskeletal disorders and Neoplasms are considered as diseases of more developed countries but  Maternal and neonatal disorders and Respiratory infections and tuberculosis are diseases that are more prevalent in less developed countries. <br> 

The following graphs show these measures and the evolution of the countries over the years. <br>
We have also expressed the economic situation of the country by its GDP per capita, which is represented by the size of the spheres. Furthermore, the the region and geographical sub-region of the specific country is represented by the colour.

{% include eco1.html %}

{% include eco2.html %}

{% include eco3.html %}

{% include eco4.html %} 

{% include eco5.html %}

Also note that nuances exist for certain geographical areas 

Notice, for example, that the countries of the Middle East and the Golf have the economic characteristics of the more developed countries but that they share the medical characteristics of the less developed countries. 

A deeper analysis of the political and medical model of these countries would be interesting for a deeper analysis of the situation. 


##### Risk factors

To better understand the risks factors for the worlds most deadliest disease, cardiovascular diseases, we analyse a dataset from [Kaggle](https://www.kaggle.com/sulianova/cardiovascular-disease-dataset) . This dataset containes data for ***70,000*** patients each described by ***11*** features: <br> age, gender, height, weight, ap_hi (systolic blood pressure), ap_lo (diastolic blood pressure), cholesterol, gluc (glucose), smoke (binary), alco (binary acohol use), active (binary exercise). 

<p align="center">
<img src="assets/correlation.png" width="550px" >
</p>

The dataset was first extensively cleaned as it contained many unrealistic values. Next some of the features were editted, height and weighted were merged into a new feature "BMI" which may be more interesting when describing cardiovascular disease as it is stronger related to diet or other health issues like diabetes.

A randomized decision tree algorithm was applied to quantify to quantify the importance of the features and thus giving us a better view of which are the biggest risk factors for cardiovascular disease.

{% include CV.html %}

We conclude that ageing is the largest contributing risk factor when it comes to cardiovascular diseases. This nicely agrees with finding in scientific literature which show that elastin proteins in the arteries degrade over time which the body cannot repair. Thus there is a direct relation between the passing of time (ageing) and cariovascular disease.

High blood pressure is a result of other factors: ageing (arterial stiffening), cholesterol levels, salt/fluid intake, ...
So in order to minimize our risk of cardiovascular disease we should try to keep our BMI and cholesterol levels as low as possible.
This can both be done be following a healthy diet and working out (burning fat).





##### conclusion




---
__Authors:__ Nathan Sennesael, Ruben Janssens, Aurelien Gabriel Debbas, Joakim Kattelus

The project was a part of the Applied Data Analysis (ADA) course at EPFL. <br>
__Instructor__: Robert West

__Special thanks to:__ <br>
__TA:__ Tiziano Piccardi<br>
__AE:__ Yves Rychener<br>
 <br>
The code and data used in the making of this data story can be found on our [GitHub](https://github.com/Senneschal/Data_Science_Alliance).
