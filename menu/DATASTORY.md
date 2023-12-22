---
layout: page
title: Prelude
permalink: /datastory
---

<style>
    .styled-table {
        border-collapse: collapse;
        margin: 25px 0;
        font-size: 0.9em;
        font-family: sans-serif;
        min-width: 400px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
        border-radius: 5px 5px 5px 5px;
        overflow: hidden
    }

    .styled-table thead tr {
        background-color: #e38b11;
        color: #ffffff;
        text-align: left;
    }

    .styled-table th,
    .styled-table td {
        padding: 3px 11px;
    }

    .styled-table tbody tr {
        border: none;
        border-bottom: 1px solid #dddddd;
    }

    .styled-table tbody tr.active-row {
    font-weight: bold;
    color: #b84d14;
    }

    .pils-cell {
        background-color: rgba(254,204,96,0.5);
    }

    .brique-cell {
        background-color: rgba(250,145,36,0.5);
    }

    .marron-cell {
        background-color: rgba(102,37,6, 0.5);
    }

/* #################################################################
Styles communs, similaires à .styled-table mais sans tr:last-of-type 
*/



.styled-table-no-last-tr {
    /* Styles communs, similaires à .styled-table mais sans tr:last-of-type */
    border-collapse: collapse;
    font-size: 0.7em;
    font-family: sans-serif;
    min-width: 100px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
    border-radius: 5px 5px 5px 5px;
    overflow: hidden;
}

.styled-table-no-last-tr thead tr {
    /* Styles pour l'en-tête */
    background-color: #e38b12;
    color: #ffffff;
    text-align: left;
}

.styled-table-no-last-tr th,
.styled-table-no-last-tr td {
    /* Styles pour les cellules */
    text-align: center;
    padding: 2.5px 10px;
}

.styled-table-no-last-tr tbody tr {
    /* Styles pour les lignes du corps du tableau */
    border: none;
    border-bottom: 1px solid #dddddd;
}

.styled-table-no-last-tr tbody tr.active-row {
    /* Styles pour les lignes actives du corps du tableau */
    font-weight: bold;
    color: #b84d14;
}

.styled-table-no-last-tr th {
    /* Styles pour les cellules d'en-tête */
    background-color: #ffffff;
}

.styled-table-no-last-tr tbody tr:last-child {
    /* Supprimer la bordure de la dernière ligne */
    border-bottom: none;
}

/* #################################################################
Styles communs, similaires à .styled-table mais taille réduite pour les graphs d'acroissement 
*/

.styled-table_small {
        border-collapse: collapse;
        margin: 25px 0;
        font-size: 0.7em;
        font-family: sans-serif;
        width: 300px;
        height: 200px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
        border-radius: 5px 5px 5px 5px;
        overflow: hidden
    }

    .styled-table_small thead tr {
        background-color: #e38b11;
        color: #ffffff;
        text-align: left;
    }

    .styled-table_small th,
    .styled-table_small td {
        padding: 8px 11px;
    }

    .styled-table_small tbody tr {
        border: none;
        border-bottom: 1px solid #dddddd;
    }

    .styled-table_small tbody tr.active-row {
    font-weight: bold;
    color: #b84d14;
    }


</style>

<div style="text-align: justify;">
In this datastory, we will try to understand which beer styles are popular, but also factors that favored their popularity. To do so, we will use data from two major rating websites from the Beeriverse, <a href="https://www.beeradvocate.com/" target="_blank">BeerAdvocate</a> and <a href="https://www.ratebeer.com/" target="_blank">RateBeer</a>. These websites populate the Beeriverse with more than 100 beer styles, thousands of beers and millions of reviews. The reviews span from the early 2000’s to 2017 and consist of grades given by the reviewer and an optional text describing their opinion.
</div>

# What styles of beers are popular?  

### Beer style analysis

<div style="text-align: justify;">
After years of continuous progress in the pursuit of crafting the finest beers, a lot of styles emerged, increasing the size of the Beeriverse up to more than 100 styles. But are all these beer styles equally popular ? Let’s have a look at distribution of ratings and number of beers per beer style.
</div>

<!-- Distribution of number of beers per beer style  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/nbr_beers_per_style_690px.html" width="700px" height="620px"></object>



<div style="text-align: justify;">
We see that several IPAs are greatly represented on both websites as well as Pale Ales and Stouts. <br>
Moreover, some styles share similarities like Imperial Stout and Stout. Hence, we opted to consolidate styles into broader categories. We drew inspiration from the <a href="https://www.beeradvocate.com/beer/styles/" target="_blank">BeerAdvocate</a> website, which has already established some "bigger style" groupings; we now have a total of fifteen larger styles. This approach enables us to present a more streamlined version of the Beeriverse for enhanced visualization.
</div>


<!-- Distribution of ratings per bigger style  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/nbr_beers_690px.html" width="700px" height="620px"></object>


<div style="text-align: justify;">
From this plot, it's evident that specific beers attract more attention than their counterparts, notably India Pale Ales, Pale Ales, Pale Lager, Strong Ales and Stouts. Notably, Indian Pale Ales (IPAs) stand out prominently, accumulating almost 3 million ratings. This leads us to ponder: could IPA be the Beeriverse messiah? <br>
</div>

<div style="text-align: justify;">
To delve deeper into Beeriversers' sentiments toward these discernible beer styles from the previous graph, we conducted a quantitative analysis by comparing the mean grades assigned to each style using Tukey's HSD test.
</div>


### Heat map


<select id="heat">
    <option value="ba_IPA">BeerAdvocate</option>
    <option value="rb_IPA">RateBeer</option>
</select>

<!-- Conteneur pour afficher le contenu sélectionné -->
<div id="heatcont">
    <!-- Le contenu sera affiché ici -->
</div>

<!-- Inclusion du script JavaScript -->
<script>
document.addEventListener('DOMContentLoaded', function() {
    const select = document.getElementById('heat');
    const content = document.getElementById('heatcont');


        function loadBeerAdvocateImage() {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_heatmap_690px.html" style="width: 700px; height: 620px;"></object>';
        }

        // Charger l'image BeerAdvocate au chargement initial
        loadBeerAdvocateImage();


    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_heatmap_690px.html" style="width: 700px; height: 620px;"></object>';
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_heatmap_690px.html" style="width: 700px; height: 620px;"></object>';
        }
    });
});
</script>

<div style="text-align: justify;">
On these heatmaps, we can observe that every beer style has a mean significantly different from other beer styles. What is interesting is the value of Meandiff for a given cell. A positive value signifies that the beer style defining the line has a higher mean than the beer style defining the column and vice versa. What we can observe is that IPAs have slightly lower grades than Pale Lagers and Pale Ales, however these differences are not as large as differences observed between other styles with Pale Lagers and Pale Ales. Given that it is complicated to draw meaningful conclusions from this simple test, we will explore more creative metrics to try to quantify IPAs popularity.
</div>



### Language analysis

<div style="text-align: justify;">
Let’s see what the Beeriversers from BeerAdvocate think of this by looking at their reviews. First of all, we have found that 99.99% of the comments on both sites are written in English, so we can ignore other languages in our future analysis. Below you can observe word clouds obtained with text from positive (grade&gt;4) and negative (grade&lt;1.5) reviews, as well as reviews for IPAs and Stouts. We compare IPAs and Stouts as these are two beer types with very different characteristics and we might be able to observe interesting discrepancies.
</div>




<div style="display: flex; justify-content: center;">
    <div style="width: 80%;">
        <div style="display: flex; justify-content: space-between;">
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/good.png" alt="Image 1" style="width: 100%; height: auto;">
                <figcaption style="text-align: center;">Good reviews</figcaption>
            </div>
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/bad.png" alt="Image 2" style="width: 100%; height: auto;">
                <figcaption style="text-align: center;">Bad reviews</figcaption>
            </div>
        </div>
    </div>
</div>


<div style="text-align: justify;">
<br>
Let’s observe words that are highly represented in positive reviews, but not in negative reviews. We can notice the presence of interesting words such as “nice”, “malt”, “hops” or “carbonation”. We can hypothesize that these words represent beer characteristics that are appreciated. For example we can see that malts and hops content are factors influencing Beeriversers appreciation towards a beer (even more considering that these words are quite small in the bad reviews word cloud).
</div>


<div style="display: flex; justify-content: center;">
    <div style="width: 80%;">
        <div style="display: flex; justify-content: space-between;">
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/ipa.png" alt="Image 3" style="width: 100%; height: 350px;">
                <figcaption style="text-align: center;">IPA reviews</figcaption>
            </div>
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/stout.png" alt="Image 4" style="width: 100%; height: 355px;">
                <figcaption style="text-align: center;">Stout reviews</figcaption>
            </div>
        </div>
    </div>
</div>


<div style="text-align: justify;">
<br>
Looking at the words most frequently mentioned in comments on IPAs, we can identify that these are notoriously hoppy, represented by "hops" and "hop" in the first 3 words. This might be a factor explaining the IPA popularity, since people seem to enjoy beers with hoppy characteristics. We can also notice the presence of the word “nice” that seems to be a good indicator of a beer's popularity. In contrast, we cannot find any word associated exclusively with bad reviews, such as “bad” or “water”. These observations suggest that in general, IPAs are quite appreciated by Beeriversers. <br>

Then, if we take a look at Stout reviews, we see that many words found in stout reviews are exclusive to stouts. This may come as surprising, as we saw that stouts seemed to be quite popular given the number of ratings they received. However, considering that stouts have a unique taste, very different from other beers, it makes sense that the vocabulary used to describe them is also unique.
<br>
</div>

<div style="display: flex; justify-content: center;">
    <table class="styled-table">
        <thead>
            <tr>
                <th>Good Reviews</th>
                <th>Bad Reviews</th>
                <th>IPA Reviews</th>
                <th>Stout Reviews</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Head</td>
                <td>Head</td>
                <td class="pils-cell">Hops</td>
                <td class="marron-cell">Chocolate</td>
            </tr>
            <tr>
                <td class="brique-cell">Nice</td>
                <td>Light</td>
                <td>Head</td>
                <td>Dark</td>
            </tr>
            <tr>
                <td>Good</td>
                <td>Smeel</td>
                <td class="pils-cell">Hop</td>
                <td class="marron-cell">Coffee</td>
            </tr>
            <tr>
                <td class="brique-cell">Dark</td>
                <td>Bottle</td>
                <td class="pils-cell">Nice</td>
                <td>Head</td>
            </tr>
            <tr>
                <td>Sweet</td>
                <td>Bad</td>
                <td>Citrus</td>
                <td class="marron-cell">Black</td>
            </tr>
            <tr>
                <td class="brique-cell">Malt</td>
                <td>Good</td>
                <td class="pils-cell">Malt</td>
                <td class="marron-cell">Roasted</td>
            </tr>
            <tr>
                <td>Light</td>
                <td>Drink</td>
                <td>Good</td>
                <td>Nice</td>
            </tr>
            <tr>
                <td class="brique-cell">Hops</td>
                <td>Flavor</td>
                <td>Orange</td>
                <td>Good</td>
            </tr>
            <tr>
                <td class="brique-cell">Well</td>
                <td>Water</td>
                <td>White</td>
                <td>Sweet</td>
            </tr>
            <tr>
                <td class="brique-cell">Carbonation</td>
                <td>Even</td>
                <td>Light</td>
                <td class="marron-cell">Brown</td>
            </tr>
        </tbody>
    </table>
</div>

<!-- Trois lignes avec les couleurs spécifiées -->
<div style="display: flex; justify-content: center; margin-top: 10px; margin-bottom: 100px;">
    <div style="background-color: rgba(250,145,36,0.5); width: 200px; height: 5px; margin-right: 10px; text-align: center;">Words that appear in good reviews but not in bad ones</div>
    <div style="background-color: rgba(254,204,96,0.5); width: 200px; height: 5px; margin-right: 10px; text-align: center;">Words found only in good and IPA reviews</div>
    <div style="background-color: rgba(102,37,6, 0.5); width: 200px; height: 5px; text-align: center;">Words exclusive to stout reviews</div>
</div>


<div style="text-align: justify;">
Now that we have the intuition that the IPA is a popular beer style, let’s try to dive deeper in the analysis. Even though tales about this style have been around for a long time, it seems that recently they are on many Beeriversers lips. Let’s confirm that by looking at the distribution of ratings per beer style in the past decades for the favorite beers. These were the beers that had a grade and score bigger than 75% of all beers.
</div>

<select id="selector2">
    <option value="ba_IPA">BeerAdvocate</option>
    <option value="rb_IPA">RateBeer</option>
</select>

<!-- Conteneur pour afficher le contenu sélectionné -->
<div id="content_ratings_per_year">
    <!-- Le contenu sera affiché ici -->
</div>

<!-- Inclusion du script JavaScript -->
<script>
document.addEventListener('DOMContentLoaded', function() {
    const select = document.getElementById('selector2');
    const content = document.getElementById('content_ratings_per_year');


        function loadBeerAdvocateImage() {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_normalized_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
        }

        // Charger l'image BeerAdvocate au chargement initial
        loadBeerAdvocateImage();


    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_normalized_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_normalized_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
        }
    });
});
</script>



<div style="text-align: justify;">
It is only now that we look at this graph that we understand how much IPAs have taken over the Beeriverse. Since 2004, the number of rated IPAs hasn’t stopped growing, up to the point where, in 2017, more than 40% of beer rated were IPAs. Interestingly they started to be popular at the same time as stouts, however stouts made astonishing debuts, only to be slowly taken over by IPAs in the past years. Among other beers Strong Ales also stand out, but it seems that their popularity peaked in the early 2000 and since subsequent ratings have shown a gradual decline.
</div>



<div style="text-align: justify;">
Furthermore, having a closer look of the year-on-year rating increments we see that IPAs again showed the sharpest rise for 16 years. One might notice the astonishing growth of Pale Ales starting in 2010, potentially shaking up the Beeriverse.
</div> 

<select id="selector10">
    <option value="ba_IPA">BeerAdvocate</option>
    <option value="rb_IPA">RateBeer</option>
</select>

<!-- Conteneur pour afficher le contenu sélectionné -->
<div id="content10">
    <!-- Le contenu sera affiché ici -->
</div>


<script>
document.addEventListener('DOMContentLoaded', function() {
    const select = document.getElementById('selector10');
    const content = document.getElementById('content10');

    function loadBeerAdvocateImage() {
        content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_increase_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
    }

    function loadBeerAdvocateTable() {
        const tableContent = `
            <div style="display: flex; justify-content: center;">
                    <table class="styled-table_small">
                        <thead>
                            <tr>
                                <th>Style</th>
                                <th style="text-align: center;">Mean increase per year:</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>India Pale Ales: </td>
                                <td style="text-align: center;"><strong>217.70%</strong></td>
                            </tr>
                            <tr>
                                <td>Pale Ales: </td>
                                <td style="text-align: center;"><strong>610.90%</strong></td>
                            </tr>
                            <tr>
                                <td>Stouts: </td>
                                <td style="text-align: center;"><strong>129.22%</strong></td>
                            </tr>
                            <tr>
                                <td>Strong Ales: </td>
                                <td style="text-align: center;"><strong>120.00%</strong></td>
                            </tr>
                            <tr>
                                <td>Wild/Sour Beers: </td>
                                <td style="text-align: center;"><strong>107.95%</strong></td>
                            </tr>
                        </tbody>
                    </table>
                </div>`;
        content.insertAdjacentHTML('beforeend', tableContent);
    }

    function loadRateBeerTable() {
        const tableContent = `
            <div style="display: flex; justify-content: center;">
                    <table class="styled-table_small">
                        <thead>
                            <tr>
                                <th>Style</th>
                                <th style="text-align: center;">Mean increase per year:</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>India Pale Ales: </td>
                                <td style="text-align: center;"><strong>280.78%</strong></td>
                            </tr>
                            <tr>
                                <td>Porters: </td>
                                <td style="text-align: center;"><strong>92.28%</strong></td>
                            </tr>
                            <tr>
                                <td>Stouts: </td>
                                <td style="text-align: center;"><strong>68.07%</strong></td>
                            </tr>
                            <tr>
                                <td>Strong Ales: </td>
                                <td style="text-align: center;"><strong>93.21%</strong></td>
                            </tr>
                            <tr>
                                <td>Wild/Sour Beers: </td>
                                <td style="text-align: center;"><strong>81.40%</strong></td>
                            </tr>
                        </tbody>
                    </table>
                </div>`;
        content.insertAdjacentHTML('beforeend', tableContent);
    }

    // Chargement initial
    loadBeerAdvocateImage();
    loadBeerAdvocateTable();

    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_increase_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
            loadBeerAdvocateTable();
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_increase_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
            loadRateBeerTable()
        }
    });
});
</script>


## Geographical analysis

<div style="text-align: justify;">
Now, let's delve into some geography.
With our conviction that IPA is the style of the moment in the Beeriverse, let’s try to understand how this happened. What were the key factors of this explosion?  
First of all, let’s see if we can identify a pattern at the scale of the world by displaying the IPA ratings  for each years.
</div>

<select id="selector">
    <option value="ba_IPA">BeerAdvocate</option>
    <option value="rb_IPA">RateBeer</option>
</select>

<!-- Conteneur pour afficher le contenu sélectionné -->
<div id="content">
    <!-- Le contenu sera affiché ici -->
</div>

<!-- Inclusion du script JavaScript -->
<script>
document.addEventListener('DOMContentLoaded', function() {
    const select = document.getElementById('selector');
    const content = document.getElementById('content');


        function loadBeerAdvocateImage() {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap_690px.html" style="width: 700px; height: 620px;"></object>';
        }

        // Charger l'image BeerAdvocate au chargement initial
        loadBeerAdvocateImage();


    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap_690px.html" style="width: 700px; height: 620px;"></object>';
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_IPA_worldmap_690px.html" style="width: 700px; height: 620px;"></object>';
        }
    });
});
</script>




<div style="text-align: justify;">
It is interesting to note that although IPAs are an English invention, they started to develop in the USA. In fact, before 2010, IPAs were almost exclusively rated in Canada and the U.S. After that, the trend started to spread to Europe, while remaining at its peak in America.
As the density of ratings is enormous in the U.S., we shall have a closer look at what is happening there to understand if any state was influential in the IPAs explosion. Here we will only look at BeerAdvocate, as RateBeer's data is more European focused.
</div>

<!-- US STATE  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_USAmap_690px.html" width="700px" height="620px"></object>



<div style="text-align: justify;">
Examination of the map reveals that from 2009 to 2013 California and Pennsylvania, located on opposite coasts of the US, have significantly influenced the development of IPAs in the country.  
They were the only two states with more than 100 ratings in 2009 and were only caught up in 2013 by very large states such as New York, Massachusetts or Illinois. We can even hypothesize that, once IPAs gained popularity in states that had similarities with Europe (such as Massachusetts and New-York), IPAs started to gain popularity on the old continent.
<br>
However, one undeniable observation from this map is that California and Pennsylvania serve as the epicenter of IPA development. The trend then spread up the north-east coast and eventually crossed the Atlantic to reach European populations.
</div>


## Social perspective
### Fanbase

<div style="text-align: justify;">
Geography alone is not enough to explain the boom of IPAs, because if a trend can spread from state to state and country to country, there must be underlying factors that explain why IPAs have conquered the hearts of the Beeriversers at lightspeed. A social aspect comes into play, the behavior of the Beeriversers. One might distinguish a normal Beeriverser and a fan, known as a BeerAficionado. A fan is defined as someone who gives more ratings than 75% of the users.<br>
In the case of a beer trend, we want to look at fan groups and their preferred style of beer. We noticed that some Beeriversers were present on both sites and decided to keep their comments on only one of them to avoid duplicates. The following graph shows the combined fan base of both sites.
</div>

<!-- FAN FOR EACH BEER STYLE  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/nbr_fans_per_style_690px.html" width="700px" height="620px"></object>

<div style="text-align: justify;">
It's evident that IPA stands out as the preferred style among fans, showing a great enthusiasm for this type of beer. Additionally, Pale Lagers and Stouts also constitute big fanbases. 
But where do these BeerAficionados come from ? As mentioned, before the trend of IPA started in the United States. However, is it due to the country’s extensive brewery count and diverse beer styles ? Alternatively, could it be that the IPA fans are American ?
</div>

<object type="text/html" data="{{ site.baseurl }}/assets/plots/fan_IPA_worldmap_690px.html" width="700px" height="620px"></object>


<div style="text-align: justify;">
The BeerAficionados of IPA are primarily situated in the US. Now there is no doubt: the IPA trend exists and originated in the United States. Its American fanbase certainly played a pivotal role in initiating this trend.
</div>



### Microbreweries

<div style="text-align: justify;">
Another interesting aspect of a beer trend revolves around the breweries themselves. Not only can we differentiate large-scale factories from microbreweries based on their size, but their mentalities also set them apart. While larger beer factories prioritize product consistency and mass production, microbreweries prefer quality, flavor diversity, and unique recipes playing with different ingredients and techniques. The trend of microbreweries originated in the 80s in the United States and the United Kingdom. The term later evolved in the 20s into ‘Craft brewery’. Thus, could this trend be linked to our IPA trend ? 
To answer this question, let’s do some language processing and take a look at the reviews that speak about microbreweries. 
</div>


<!-- Image Microbrewery IPA overall  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/microbrewery_ipa_overall.html" width="700px" height="520px"></object>

<div style="text-align: justify;">
In this analysis, we observe that the proportion of IPA reviews mentioning microbreweries is higher than the percentage of reviews discussing microbreweries across all beer styles. In fact there are only Pale Ales that seem to show the same affinity with the microbrewing culture as IPAs.
</div>


<div style="display: flex; justify-content: center; margin-top: 30px;">
    <table class="styled-table-no-last-tr">
        <tbody>
            <tr>
                <th class="first-column">Chi-square statistic:</th>
                <td>853.347</td>
            </tr>
            <tr>
                <th class="first-column">P-value:</th>
                <td>1.361e<sup>-187</sup></td>
            </tr>
        </tbody>
    </table>
</div>

<div style="text-align: justify;">
This difference in percentage was statistically different indicating a strong association between IPAs and microbreweries. This might suggest the contribution of a trend to the emergence and growth of another one. <br>
In our case, the connection between IPAs and the already popular microbreweries could have played a role in fostering or influencing the growth of the IPA trend.
</div>



## Prediction of the next trendy beer

<div style="text-align: justify;">
As many wise Beeriversers reading our story, you probably cannot stop but wondering about the next trendy hoppy beverage. We were also puzzled by that question and tried to predict the course of the Beeriverse. We made the assumption that a beer as groundbreaking as IPAs should share some similar characteristics with it. The extent of such similarities might be out of our reach, hidden in the mysteries of the Beeriverse. To identify it more clearly we came across an Ale-chemist that provided us with dark potions labeled as feature selection and DBSCAN. It first helped us to narrow down the number of characteristics associated with beer styles. We then managed to group them according to their resemblance and obtained the following graph.  
</div>


## Conclusion

Our journey through the Beeriverse comes to an end. We've been able to dissect popular beer styles and unravel the underlying factors dictating their popularity.
One of the highlights of our analysis showed that IPAs have emerged as a dominant force, captivating the hearts of beer lovers the world over. The enthusiasm of beer lovers for IPAs, particularly in the USA, attests to the origin and growth of this trend.<br>

Beyond geographical frontiers, social dynamics have come into play, highlighting the distinction between occasional beer lovers and fervent fans. These BeerAficionados, with their penchant for IPAs, Pale Lagers and Stouts, marked a turning point in the beer landscape. They brought their favorite beverages on a whole other level of popularity.<br>

We also came upon locations where beer lovers in a quest for new flavors would meet. We investigated the role of microbreweries and we discovered that they seem to offer a platform for IPAs, bringing their name out in the world.<br>

Finally, we tried to identify the magic recipe that led to IPA popularity and tried to predict the future of the Beeriverse. Pale Ales CHECK were found to be the most likely groundbreaking beer style. <br>

Overall, the History of Beer is a fascinating journey through time, mixing history, people and flavors into the amazing world of beer, the Beeriverse. The evolution of our lifestyles and tastes has shaped and will continue to shape this incredible beverage, like a never-ending story. <br>
