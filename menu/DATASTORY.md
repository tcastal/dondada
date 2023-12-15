---
layout: page
title: "Brewmageddon: How IPAs Took Over the Beeriverse"
permalink: /datastory
---

En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.
En remplaçant la balise <h1> par <p>, le texte sera désormais formaté comme un paragraphe au lieu d'un titre de premier niveau. Cela changera la sémantique de la balise et le rendra visuellement différent, mais le texte restera là où vous l'avez placé dans votre code HTML.


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
