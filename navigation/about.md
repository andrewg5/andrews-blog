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
<br>
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    
var living_in_the_world = [
    {"flag": "2/2e/Flag_of_China.png", "description": "China - Where my parents are from. Most of my relatives live there and I vist often"},
    {"flag": "0/01/Flag_of_California.svg", "description": "California - I have lived in California for my whole life"},

];
 
    
    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>


## Here are some things that I enjoy

<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/tennis.png" alt="Tennis">
  <img src="{{site.baseurl}}/images/about/cyberpatriot.png" alt="Cyberpatriot">
  <img src="{{site.baseurl}}/images/about/terraria.png" alt="Terraria">
  <img src="{{site.baseurl}}/images/about/vs.png" alt="Visual Studio">
  <img src="{{site.baseurl}}/images/about/mazerunner.png" alt="Maze Runner Book">
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