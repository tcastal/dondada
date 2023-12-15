---
layout: home
title: Contact
permalink: /contact
---

<div class="gallery">
    <div class="image">
        <img src="{{ site.baseurl }}/assets/img/Adrien.jpeg">
        <p>Adrien Sizaret</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_2.jpg">
        <p>Margot Chapot</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_3.jpg">
        <p>Thibaut Haslé</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_4.jpg">
        <p>Gaspard Oudinot</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_5.jpg">
        <p>Thomas Castaldi</p>
    </div>
</div>


<style>
.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-left: -50px; /* Compenser l'espacement négatif pour aligner avec le container */
    margin-right: 50px; /* Compenser l'espacement négatif pour aligner avec le container */
}

.image {
    width: 18%;
    margin-bottom: 20px; /* Espacement en bas de chaque image */
    text-align: center;
    margin-right: 10px; /* Espacement horizontal entre les images */
}

.image:last-child {
    margin-right: 0; /* Supprime l'espacement à droite de la dernière image */
}


.image img {
    width: 100%;
    height: auto;
    border-radius: 50%;
}

.image p {
    margin-top: 5px;
    font-size: 14px;
}
</style>
