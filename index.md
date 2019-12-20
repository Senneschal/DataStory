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

##### Risk factors

##### Economical and political factors

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
