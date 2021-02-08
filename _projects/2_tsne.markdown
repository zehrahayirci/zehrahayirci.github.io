---
layout: page
title: instagram TSNE 
date: 2021-01-03 15:25
description : TSNE visualization of instagram posts
img: assets/img/insta_histogram2.png
importance: 2 
---

[t-SNE](https://lvdmaaten.github.io/tsne/) is a popular dimension reduction algorithm. Why not try to use it on instagram posts!

This notebook best work in Google Colab, and don't forget to enable GPU from Edit -> Notebook Settings -> Hardware

I use [Jonker-Volgenant algorithm](https://blog.sourced.tech/post/lapjv/) to create a nice grid for instagram!

[My instagram](https://www.instagram.com/days.of.zehra/) with Histogram t-SNE

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/insta_histogram2.png' | relative_url }}" >
    </div>
</div>
<br>

1500 images of cats, dogs and bears using their histogram


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/histogram_tsne_32.png' | relative_url }}" >
    </div>
</div>
<br>

Using their pretrained ImageNet features


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/tsne_features2.png' | relative_url }}" > 
    </div>
</div>
<br>
Using both histogram and pretrained fetures

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/tsne_all2.png' | relative_url }}" > 
    </div>
</div>
<br>
All the codes in this [repo](https://github.com/zehrahayirci/instagram_t-SNE)

Read the [t-SNE pape](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf), watch Van der Maaten's [Google Talk](https://www.youtube.com/watch?v=RJVL80Gg3lA) or check the examples on [his blog](https://lvdmaaten.github.io/tsne/)


Inspired from Prabodh Tripathi's [blog post](https://thebittheories.com/t-sne-visualization-of-instagram-posts-d5915ae99e63)

