---
layout: page
title: "Brewmageddon: How IPAs Took Over the Beeriverse"
permalink: /datastory
---
## Setting the scene

<div style="text-align: justify;">
Beer is one of the oldest human-producest drinks. At the dawn of Beeriverse, about 8 thousand years ago, humans in Mesopotamia produced a drink by fermenting bread. If one of us drinked it nowadays, we would probably find the taste awful. Later, during the middle age, people in Germany started to cultivate hops, which flower can be used to adjust beer flavor and bitterness. Then, in the past centuries, what was just a simple beverage with plain taste eventually evolved with the humans that produced it. For example porters were brewed for cargo carriers working in the cold londonian environment, while trappist monks in belgium who used to produce everything they consumed developed a taste for strong “tripel” beers. These two examples are but a glimpse of the many styles of this godly beverage that were created and how they were influenced by many geographical and social factors. <br>

So embark on a journey to discover which style will win the battle to claim the title of most popular beer style of the Beeriverse.
</div>

## Introduction

We will try to understand which beer styles are popular, but also factors that favored their popularity. To do so, we will use data from two major rating websites from the Beeriverse, BeerAdvocate and RateBeer. These websites populate the Beeriverse with more than 100 beer styles, thousands of beers and millions of reviews. The reviews span from the early 2000’s to 2017 and consist of grades given by the reviewer and an optional text describing their opinion.

## What styles of beers are popular?

After years of continuous progress in the pursuit of crafting the finest beers, a lot of styles emerged, increasing the size of the Beeriverse up to more than 100 styles. To enhance visual clarity, we will display only the fifteen largest numbers of beers and ratings for each style of beers.



**ADD PLOT**


<div style="display: flex; justify-content: center;">
    <div style="width: 80%;">
        <div style="display: flex; justify-content: space-between;">
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/image1.png" alt="Image 1" style="width: 100%; height: auto;">
            </div>
            <div style="width: 45%;">
                <img src="{{ site.baseurl }}/assets/plots/image2.png" alt="Image 2" style="width: 100%; height: auto;">
            </div>
        </div>
    </div>
</div>


### Row 2

<div style="text-align: center;">
    <div style="display: inline-block; width: 45%; margin: 0 2.5%;">
        <img src="{{ site.baseurl }}/assets/plots/image1.png" alt="Image 1" style="width: 100%; height: auto;">
    </div>
    <div style="display: inline-block; width: 45%; margin: 0 2.5%;">
        <img src="{{ site.baseurl }}/assets/plots/image2.png" alt="Image 2" style="width: 100%; height: auto;">
    </div>
</div>







Certain beers, such as India Pale Ale (IPA), American IPA, and Pale Ale (APA), stand out from others. Moreover, there are styles that share similarities like Imperial Stout and Stout. Hence, we opted to consolidate styles into broader categories.We drew inspiration from the BeerAdvocate website, which has already established some "bigger style" groupings; we now have a total of fifteen larger styles. This approach enables us to present a more streamlined version of the Beeriverse for enhanced visualization.



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
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap_700px.html" style="width:100%; height:100%; overflow:hidden;"></object>';
        }

        // Charger l'image BeerAdvocate au chargement initial
        loadBeerAdvocateImage();


    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap_700px.html" width="750px" height="650px"></object>';
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_IPA_worldmap.html" width="100%" height="600px"></object>';
        }
    });
});
</script>

Comment ?
