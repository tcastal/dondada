---
layout: home
title: Contact
permalink: /contact
---
<style>
    #imagesMain {
        padding: 0;
        margin-left: 20px;
        margin-right: 20px;
        margin-top: 100px;
        text-align: center;
        display: flex; /* Utilisation de flexbox */
        justify-content: center; /* Centrer horizontalement */
    }
    .image-container {
        margin-right: 20px; /* Espacement entre les images */
    }
    .image-container:last-child {
        margin-right: 0; /* Aucun espacement à droite pour la dernière image */
    }
    #imagesMain img {
        height: 100px;
        width: 100px;
        vertical-align: middle;
    }
</style>

<div id="imagesMain">
    <div class="image-container">
        <img src="{{ site.baseurl }}/assets/img/Adrien.png">
        <p>Adrien</p>
    </div>
    <div class="image-container">
        <img src="{{ site.baseurl }}/assets/img/Thibaut.png">
        <p>Thibaut</p>
    </div>
    <div class="image-container">
        <img src="{{ site.baseurl }}/assets/img/Margot.png">
        <p>Margot</p>
    </div>
    <div class="image-container">
        <img src="{{ site.baseurl }}/assets/img/Thomas.png">
        <p>Thomas</p>
    </div>
        <div class="image-container">
        <img src="{{ site.baseurl }}/assets/img/Gaspard.png">
        <p>Gaspard</p>
    </div>
</div>





<div style="text-align: center; font-weight: bold;">
    Disclamer: alcohol abuse is dangerous for your health, consume with moderation.
</div>

<script>
    document.addEventListener('contextmenu', event => {
        // Empêche le menu contextuel uniquement sur cette page
        event.preventDefault();
    });
</script>