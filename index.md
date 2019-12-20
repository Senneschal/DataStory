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

We find that cardiovascular disease and cancer are globaly by far the most common causes of death, thus are these two disease will be in our main interest. However, the causes of death strongly vary between different countries. <br>
Now let's visualize how the mortality of individual diseases compare between countries on a world map.

{% include 1.1.2.html %}

For cardiovascular disease, in general, we see that it is becoming more prevelent in developing countries while its prevelence is decreasing in developed countries. Note that Syria is a clear outlier in the Middle East, this may very well be a result of war.

The Global Burden of Diseases dataset also contains a number of other interesting measures to see the impact of diseases on people's quality of life.

{% include comp_of_measures.html %}

##### Clustering

Hello Joakim

{% include cluster1.html %}

COMMENT: This plot shows strong difference between the Western and Eastern world, especially in Europe the grouping goes almost by the old iron curtain. This supports the hypothesis that cardiovascular diseases may depend mainly on societal and economic factors.

{% include cluster2.html %}

COMMENT: For respiraytory and tuberculosis, the correlation appears stronger, as larger groups form at lower grouping tresholds. The grouping also appears less dependant on societal and economic factors than for cardiovascular diseases, and perhaps more dependant on geography. This makes sense, as this is now an infectious disease we are looking at.

An interesting correlation that shows up is the strong correlation between Germany and Argentina. This could just be a coincidence, but there are strong historical ties between the countries and a lot of German expats/people with German roots living in Argentina. https://en.wikipedia.org/wiki/German_Argentine People may transfer the diseases from country to country when visiting relatives. We are also looking at a long term measure such as DALY's. One hypthesis that could be made is that German Argentines with dual citizenship might seek treatment in Germany, a country ranked higher in healthcare comparisons. However, more research on if this kind of phenomenon exists would be needed, as this is pure speculation at this point.

{% include cluster3.html %}

For infectious diseases, incidence might be a better measure. Indeed, looking at Incidence as opposecd to DALYs shows some interesting things: the correlations are strong, indicating an infectious disease. At high groupimg,the entire world except for a select few countries are positively correlated, while these countries actually appear negatively correlated to teh bigger group. The interesting observation that can be made is that all these countries in their own separate groups are countries that have been subject to considerable instability, strife and even civil war in the time period lookid at. (Liberia, Chad, Afghanistan...) This might indicate that the disease incidence in conflict prone countries is simialr between these countries and very different and not positively correlated with the rest of the world. In essence, these countries may be "isolated", and not part of the global network of disease transmission. However, due to strife and instability, the medical data from these countries might just be incomolete or faulty.

{% include cluster6.html %}



##### Risk factors

To better understand the risks factors for worlds most deadliest disease, cardiovascular diseases, we analyse this dataset: https://www.kaggle.com/sulianova/cardiovascular-disease-dataset. This dataset containes data for 70,000 patients each described by 11 features: <br> age, gender, height, weight, ap_hi (systolic blood pressure), ap_lo (diastolic blood pressure), cholesterol, gluc (glucose), smoke (binary), alco (binary acohol use), active (binary exercise). 

<p align="center">
<img src="assets/correlation.png" width="600px" >
</p>

The dataset was first extensively cleaned as it contained many unrealistic values. Next some of the features were editted, height and weighted were merged into a new feature "BMI" which may be more interesting when describing cardiovascular disease as it is stronger related to diet or other health issues.

A randomized decision tree algorithm was applied to quantify to quantify the importance of the features and thus giving us a better view of which are the biggest risk factors for cardiovascular disease.

{% include CV.html %}


##### Economical and political factors


We saw in the previous section that some causes of death were more significant than others. 
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
