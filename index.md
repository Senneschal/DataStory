---
feature_text: |
    # <span style="color:#333333">Globalized Analysis of Medical Data </span> 
feature_image: "./assets/world.png"
background-color: #333333
---

__This project describes the analysis to medical data in combination with data of a variety of possible influencing factors. Our goal is to extract usefull information from this data that could help improve societies quality of life. In order to maximize the potential positive influences of the performed research, it follows naturally that it may be most interesting to look at the medical data from a globalized point of view.__

##### Measures

Which diseases have the most significant negative impact on society's quality of life? <br> How does differ between countries and over time? <br>
The most severe effect of a disease is when it causes death, after all, you can't have any "quality of life" anymore if your life has come to an end. <br>

{% include Amount_of_recorded_deaths.html %}

{% include 1.1.1.html %}

We find that cardiovascular disease and cancer are globaly by far the most common causes of death, thus are these two disease will be in our main interest. However, the causes of death strongly vary between different countries. <br>
Now let's visualize how the mortality of individual diseases compare between countries on a world map.

{% include 1.1.2.html %}

For cardiovascular disease, in general, we see that it is becoming more prevelent in developing countries while its prevelence is decreasing in developed countries. Note that Syria is a clear outlier in the Middle East, this may very well be a result of war.

The Global Burden of Diseases dataset also contains a number of other interesting measures to see the impact of diseases on people's quality of life.

{% include comp_of_measures.html %}

##### Clustering

{% include cluster1.html %}

{% include cluster2.html %}

{% include cluster3.html %}

{% include cluster4.html %}

{% include cluster5.html %}

{% include cluster6.html %}



##### Risk factors

##### Economical and political factors


We saw in the previous section that some causes of death were more significant than others. 
If we add the life expectancy and the GDP per capita, we notice that the suggestions we made previously are realistic. 

Indeed, we notice that cardiovascular diseases and apply precipitously to the most developed countries and to the richest countries while other causes of death apply more to the least developed countries. 

Cardiovascular diseases, Musculoskeletal disorders and Neoplasms are considered as diseases of more developed countries but  Maternal and neonatal disorders and Respiratory infections and tuberculosis are diseases that are more prevalent in less developed countries. 

The following graphs show these measures and the evolution of the countries over the years. 


We also note that nuances exist for certain geographical areas 

We notice, for example, that the countries of the Middle East and the Golf have the economic characteristics of the more developed countries but that they share the medical characteristics of the less developed countries. 

A deeper analysis of the political and medical model of these countries would be interesting for a deeper analysis of the situation. 

The graph below shows us the prevalence of maternal and neonatal disorders in respect to life expectancy. 
We have also expressed the economic situation of the country by its GDP per capita, which is represented by the size of the spheres. Furthermore, the the region and geographical sub-region of the specific country is represented by the colour.

{% include eco1.html %}

The graph below shows us the prevalence of maternal and neonatal disorders in respect to life expectancy. 

{% include eco2.html %}

The graph below shows us the prevalence of maternal and neonatal disorders in respect to life expectancy. 

{% include eco3.html %}

The graph below shows us the prevalence of maternal and neonatal disorders in respect to life expectancy. 

{% include eco4.html %}

The graph below shows us the prevalence of maternal and neonatal disorders in respect to life expectancy. 

{% include eco5.html %}

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
