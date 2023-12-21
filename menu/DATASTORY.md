---
layout: page
title: "Brewmageddon: How IPAs Took Over the Beeriverse"
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
        background-color: rgba(254,196,79,0.3);
    }

    .brique-cell {
        background-color: rgba(236,112,20,0.3);
    }

    .marron-cell {
        background-color: rgba(149, 0, 0, 0.36);
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



# Introduction
<h1>Introduction</h1>

<div style="text-align: justify;">
In this datastory, we will try to understand which beer styles are popular, but also factors that favored their popularity. To do so, we will use data from two major rating websites from the Beeriverse, <a href="https://www.beeradvocate.com/" target="_blank">BeerAdvocate</a> and <a href="https://www.ratebeer.com/" target="_blank">RateBeer</a>. These websites populate the Beeriverse with more than 100 beer styles, thousands of beers and millions of reviews. The reviews span from the early 2000’s to 2017 and consist of grades given by the reviewer and an optional text describing their opinion.
</div>

## What styles of beers are popular?

<div style="text-align: justify;">
After years of continuous progress in the pursuit of crafting the finest beers, a lot of styles emerged, increasing the size of the Beeriverse up to more than 100 styles. But are all these beer styles equally popular ? Let’s have a look at distribution of ratings and number of beers per beer style. Note that to enhance visual clarity, we will only display the fifteen most important beer styles, not the 100 existing.
</div>



## INSERER IMAGE



<div style="text-align: justify;">
Certain beers, such as India Pale Ale (IPA), American IPA, and Pale Ale (APA), stand out from others. Moreover, there are styles that share similarities like Imperial Stout and Stout. Hence, we opted to consolidate styles into broader categories. We drew inspiration from the BeerAdvocate website, which has already established some "bigger style" groupings; we now have a total of fifteen larger styles. This approach enables us to present a more streamlined version of the Beeriverse for enhanced visualization.
</div>


## INSERER IMAGE

<div style="text-align: justify;">
From this plot, we can clearly observe that certain beers receive more attention than their counterparts. It is particularly the case for India Pale Ales, Pale Ales, Strong Ales and Stouts. Indian Pale Ales (IPAs) particularly stand out, with almost 3 millions cumulated ratings. Could IPA be the Beeriverse messiah ?  
Let’s see what the Beeriversers from BeerAdvocate think of this by looking at their reviews. Below you can observe word clouds obtained with text from positive (grade&lt;4) and negative (grade&gt;2) reviews, as well as reviews for IPAs and Stouts. You might think, why compare IPAs and stouts ? Indeed, we could have chosen to also compare IPAs and Pale Ales, but you will see later that Stouts are more interesting.
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
Now let’s look at words highly represented in reviews about IPAs. IPAs are notoriously very hoppy, which is represented by “hops” and “hop” in the top 3 words. This might be a factor explaining the IPA popularity, since people seem to enjoy beers with hoppy characteristics. We can also notice the presence of the word “nice” that seems to be a good indicator of a beer's popularity. In contrast, we cannot find any word associated exclusively with bad reviews, such as “bad” or “water”. These observations suggest that in general, IPAs are quite appreciated by Beeriversers.  

Then, if we take a look at Stout reviews, we see that many words are exclusive to stouts. This may come as surprising, as we saw that stouts seemed to be quite popular. However, considering that stouts have a unique taste, very different from other beers, it makes sense that the vocabulary used to describe them is also unique.
<br>
</div>

# TABLE INSERTION:

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
                <td>Quot</td>
                <td class="pils-cell">Hop</td>
                <td class="marron-cell">Coffee</td>
            </tr>
            <tr>
                <td class="brique-cell">Dark</td>
                <td>Smell</td>
                <td class="pils-cell">Nice</td>
                <td>Head</td>
            </tr>
            <tr>
                <td>Sweet</td>
                <td>Bottle</td>
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
                <td>Flavor</td>
                <td>Good</td>
                <td>Nice</td>
            </tr>
            <tr>
                <td class="brique-cell">Hops</td>
                <td>Sweet</td>
                <td>Orange</td>
                <td>Good</td>
            </tr>
            <tr>
                <td class="brique-cell">Well</td>
                <td>Bad</td>
                <td>White</td>
                <td>Sweet</td>
            </tr>
            <tr>
                <td class="brique-cell">Carbonation</td>
                <td>Much</td>
                <td>Light</td>
                <td class="marron-cell">Brown</td>
            </tr>
        </tbody>
    </table>
</div>





<div style="text-align: justify;">
Now that we have the intuition that the IPA is a popular beer style, let’s try to dive deeper in the analysis. Even though tales about this style have been around for a long time, it seems that recently they are on many Beeriversers lips. Let’s confirm that by looking at the distribution of ratings per beer style in the past decades.
</div>


## BARBLOT COULEUR THIB

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
It is only now that we look at this graph that we understand at what point IPAs have taken over the Beeriverse. Before 2003 IPAs were nowhere to be seen, nobody graded them. But since 2004 their share in the number of beer rated hasn’t stopped growing, up to the point where, in 2017, more than 40% of beer rated were IPAs. Interestingly they started to be popular at the same time as stouts, however stouts made astonishing debuts, only to be slowly taken over by IPAs in the past years.
</div>


## NEW GRAPH MARGOT + TABLE 

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

    // Charger l'image BeerAdvocate au chargement initial
    loadBeerAdvocateImage();
    loadBeerAdvocateTable();

    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_increase_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
            loadBeerAdvocateTable();
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_increase_ratings_690px.html" style="width: 700px; height: 620px;"></object>';
            // Tu peux charger le tableau correspondant pour RateBeer ici si nécessaire
        }
    });
});
</script>



## A bit of geography

<div style="text-align: justify;">
Now that we are convinced that IPA is the style of the moment in the Beeriverse, let’s try to understand how this happened. What were the key factors of this explosion ? First of all, let’s see if we can identify a pattern at the scale of the world by displaying the IPA ratings on for each years.
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
Interestingly, we see that even though IPAs are an english invention, it is in the U.S. that they started to develop. As a matter of fact, before 2010, IPAs received ratings almost exclusively from Canada and the U.S. After that, the trend started to spread to Europe, while remaining at its top in America.

Finalement, ce serait intéressant de regarder ratebeer ici. Parce que le peu de note européennes meme au top de la trend donne un peu un biais.  
As the density of ratings is enormous in the U.S., we should have a look at what is happening there to understand if any state were influential in the IPAs explosion.
</div>

## US STATE 

<!-- US STATE  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_USAmap_690px.html" width="700px" height="620px"></object>



<div style="text-align: justify;">
Looking at the map, it seems that two states at opposite coasts of the U.S., California and Pennsylvania played a big role in the development of IPAs in the U.S. They were the 2 only states with more than 100 ratings in 2009 and were only caught up by very big states like New-York, Massachusetts or Illinois in 2013. We can even hypothesize that, once IPAs gained popularity in states that had similarities with Europe (such as Massachusetts and New-York), IPAs started to gain popularity on the old continent.  

Nonetheless, by looking at this map, it is undeniable that California and Pennsylvania constitute the cradle of IPAs.  
</div>



## SOCIAL POINT OF VIEW

<!-- Image Microbrewery IPA overall  -->
<object type="text/html" data="{{ site.baseurl }}/assets/plots/microbrewery_ipa_overall.html" width="700px" height="520px"></object>

<div style="display: flex; justify-content: center;">
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

Reject the null hypothesis: There is a significant difference.





# TEST 

