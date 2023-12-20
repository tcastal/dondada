---
layout: page
title: "Brewmageddon: How IPAs Took Over the Beeriverse"
permalink: /
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
        background-color: #e38b12;
        color: #ffffff;
        text-align: left;
    }

    .styled-table th,
    .styled-table td {
        padding: 12px 15px;
    }

    .styled-table tbody tr {
        border: none;
        border-bottom: 1px solid #dddddd;
    }

    .styled-table tbody tr:nth-of-type(even) {
        background-color: #f3f3f3;
    }

    .styled-table tbody tr:last-of-type {
        border-bottom: 2px solid #e38b12;
    }

    .styled-table tbody tr.active-row {
    font-weight: bold;
    color: #b84d14;
    }

</style>





## Setting the scene

<div style="text-align: justify;">
Beer is one of the oldest human-producest drinks. At the dawn of Beeriverse, about 6 thousand years before B.C. (Beerus Christ), humans in Mesopotamia produced a drink by fermenting bread. If one of us drinked it nowadays, we would probably find the taste awful. Later, during the middle age, people in Germany started to cultivate hops, which flower can be used to adjust beer flavor and bitterness. Then, in the past centuries, what was just a simple beverage with plain taste eventually evolved with the humans that produced it. For example porters were brewed for cargo carriers working in the cold Londonian environment, while trappist monks in belgium who used to produce everything they consumed developed a taste for strong “tripel” beers. These two examples are but a glimpse of the many styles of this godly beverage that were created and how they were influenced by many geographical and social factors.  

So embark on a journey to discover which style will win the battle to claim the title of most popular beer style of the Beeriverse.
</div>

## Introduction

<div style="text-align: justify;">
We will try to understand which beer styles are popular, but also factors that favored their popularity. To do so, we will use data from two major rating websites from the Beeriverse, <a href="https://www.beeradvocate.com/" target="_blank">BeerAdvocate</a> and <a href="https://www.ratebeer.com/" target="_blank">RateBeer</a>. These websites populate the Beeriverse with more than 100 beer styles, thousands of beers and millions of reviews. The reviews span from the early 2000’s to 2017 and consist of grades given by the reviewer and an optional text describing their opinion.
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
            <td>Hops</td>
            <td>Chocolate</td>
        </tr>
        <tr>
            <td>Nice</td>
            <td>Light</td>
            <td>Head</td>
            <td>Dark</td>
        </tr>
        <tr>
            <td>Good</td>
            <td>Quot</td>
            <td>Hop</td>
            <td>Coffee</td>
        </tr>
        <tr>
            <td>Dark</td>
            <td>Smell</td>
            <td>Nice</td>
            <td>Head</td>
        </tr>
        <tr>
            <td>Sweet</td>
            <td>Bottle</td>
            <td>Citrus</td>
            <td>Black</td>
        </tr>
        <tr>
            <td>Malt</td>
            <td>Good</td>
            <td>Malt</td>
            <td>Roasted</td>
        </tr>
        <tr>
            <td>Light</td>
            <td>Flavor</td>
            <td>Good</td>
            <td>Nice</td>
        </tr>
        <tr>
            <td>Hops</td>
            <td>Sweet</td>
            <td>Orange</td>
            <td>Good</td>
        </tr>
        <tr>
            <td>Well</td>
            <td>Bad</td>
            <td>White</td>
            <td>Sweet</td>
        </tr>
        <tr>
            <td>Carbonation</td>
            <td>Much</td>
            <td>Light</td>
            <td>Brown</td>
        </tr>
    </tbody>
</table>










<div style="text-align: justify;">
Now that we have the intuition that the IPA is a popular beer style, let’s try to dive deeper in the analysis. Even though tales about this style have been around for a long time, it seems that recently they are on many Beeriversers lips. Let’s confirm that by looking at the distribution of ratings per beer style in the past decades.
</div>


## INSERER BARBLOT COULEUR THIB

<select id="selector1">
    <option value="ba_IPA">BeerAdvocate</option>
    <option value="rb_IPA">RateBeer</option>
</select>

<!-- Conteneur pour afficher le contenu sélectionné -->
<div id="content_ratings">
    <!-- Le contenu sera affiché ici -->
</div>

<!-- Inclusion du script JavaScript -->
<script>
document.addEventListener('DOMContentLoaded', function() {
    const select = document.getElementById('selector1');
    const content = document.getElementById('content_ratings');


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







## Number of ratings for the IPA's around the world

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

Comment ?