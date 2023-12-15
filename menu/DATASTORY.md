---
layout: page
title: "Brewmageddon: How IPAs Took Over the Beeriverse"
permalink: /datastory
---

In this exploration, we embark on a journey to uncover the meteoric rise of India Pale Ales (IPAs) within the realm of beer culture.  
While the term 'IPA' has historical roots tracing back to centuries past, its explosion in popularity has been a recent phenomenon. Today, it's nearly impossible to enter a bar without encountering this ubiquitous term adorning beer taps worldwide. But what catalyzed this unprecedented craze?

This project delves deep into unraveling the enigma surrounding the IPA's ascendancy, scrutinizing its spread across geographical and social landscapes. Through meticulous analysis of millions of reviews from esteemed beer rating websites such as BeerAdvocate and RateBeer, we aim to unearth the intricacies behind the IPA's global dominance.

Our research sets forth compelling inquiries:

- Is the IPA genuinely the supreme choice amongst beer enthusiasts, or do other beer styles trail behind in a similar trend?
- Geographically, where did this trend originate, and what pivotal regions acted as its launchpad? Are there distinctive patterns in its global dissemination?
- Can we establish a correlation between the surge of microbreweries, craft beer, and the soaring popularity of IPAs?
- From a social perspective, where does the passionate fanbase of IPAs predominantly reside? 
- Do successful breweries consistently craft trendsetting beers akin to IPAs?

Furthermore, armed with insights gained from our analysis, we aspire to forecast the next evolutionary wave in beer preference. What will succeed the IPA in the hearts of beer aficionados, and from which corner of the world will this emergence originate?

Join us in this riveting expedition through the beeriverse as we uncover the past, present, and future of beer trends, aiming to decipher the recipe behind the global dissemination of beer styles and predicting the ever-evolving preferences of beer enthusiasts.


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
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap.html" width="100%" height="600px"></object>';
        }

        // Charger l'image BeerAdvocate au chargement initial
        loadBeerAdvocateImage();


    select.addEventListener('change', function() {
        const selectedValue = select.value;
        if (selectedValue === 'ba_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/ba_IPA_worldmap.html" width="100%" height="600px"></object>';
        } else if (selectedValue === 'rb_IPA') {
            content.innerHTML = '<object type="text/html" data="{{ site.baseurl }}/assets/plots/rb_IPA_worldmap.html" width="100%" height="600px"></object>';
        }
    });
});
</script>

Comment ?


Comment ?
