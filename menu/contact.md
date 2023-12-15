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
        <p>Nom de la personne 2</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_3.jpg">
        <p>Nom de la personne 3</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_4.jpg">
        <p>Nom de la personne 4</p>
    </div>
    <div class="image">
        <img src="chemin_vers_image_5.jpg">
        <p>Nom de la personne 5</p>
    </div>
</div>

<style>

.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.image {
    width: 18%;
    margin-bottom: 20px;
    text-align: center;
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
