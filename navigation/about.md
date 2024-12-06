---
layout: page
title: About
permalink: /about/
---


<style>
    /* Style looks pretty compact, trace grid-container and grid-item in the code */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

     .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>



Hello! I'm Andrew, a freshman at DNHS.
<br>

## Here are some things that I enjoy

<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/tennis.png" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/mazerunner.png" alt="Image 2">
  <img src="{{site.baseurl}}/images/placeholder.png" alt="Image 3">
  <img src="{{site.baseurl}}/images/placeholder.png" alt="Image 4">
  <img src="{{site.baseurl}}/images/placeholder.png" alt="Image 5">
  <img src="{{site.baseurl}}/images/placeholder.png" alt="Image 6">
</div> 



## My Programming Experience
<li><b>C++<b> - 4 years
<li><b>Java<b> - 3 years
<li><b>Unity Game Engine<b> - 5 years
<li><b>Javascript<b> - 1 year
<li><b>Python<b> - 2 years

<br>
<br>
<br>


<script src="https://utteranc.es/client.js"
        repo="andrewg5/andrews-blog"
        issue-term="title"
        label="blogpost-comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>