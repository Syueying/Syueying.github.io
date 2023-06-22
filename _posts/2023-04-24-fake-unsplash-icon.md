---
layout: post
title: Fake Unsplash Icon
date: 2023-04-24
# description: Fake Unsplash icon is drown using HTML/CSS/JS, functionality of switching themes is also provided.
tags: tech html css js
# coverImage: ../assets/img/2023/04/24/fake-unsplash-icon-cover.png
---

Just for fun !

Source code can be found in [CodePen](https://codepen.io/Syueying/full/zYmGrVX) 

Layout is actually quite simple (check it out below 👇🏻). I just give it six same rectangulars which are placed in difference positions, and also a divider which is used to provide a little space between the upper part and bottom part.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/2023/04/24/icon-layout.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Oh, rihgt, you might be curious about why I am using three separate rectangulars for the third row, instead of just filling it with all black. The reason I am doing this is simple as well, I just want to add some animations on this icon in the near future, and I believe it will be cool if each rectangular has its own animation.

The final looks like:

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/2023/04/24/theme-light.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/2023/04/24/theme-dark.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Three days later (04/27)... I added some animations to make it display like it's loading something.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="/assets/img/2023/04/24/light_animation.gif" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="/assets/img/2023/04/24/dark_animation.gif" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<p style="font-weight: bold">❗️ Again, just for fun, please don’t use it for any serious reason, expecially for making money. Thanks a lot :)</p>