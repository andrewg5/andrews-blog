---
layout: base
title: Cookie Clicker
permalink: /cookie/
---

<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        margin: 0;
        padding: 0;
        background-color: #f8f8f8;
    }

    .container {
        margin-top: 50px;
    }

    .cookie {
        cursor: pointer;
    }

    .info {
        margin-top: 20px;
        font-size: 24px;
    }

    button {
        padding: 10px 20px;
        font-size: 18px;
        cursor: pointer;
        background-color: #4CAF50;
        color: white;
        border: none;
        border-radius: 5px;
        margin-top: 20px;
    }

    button:hover {
        background-color: #45a049;
    }
</style>

<body>

<div class="container">
    <h2>Cookie Clicker Game</h2>
    <img src="{{site.baseurl}}/images/cookieClicker/cookie.png" alt="cookie" id="cookie" style="cursor: pointer; width: 300px; height: auto;" >
    <div class="info">
        <p>Cookies: <span id="cookie-count">0</span></p>
        <p>Workers: <span id="worker-count">0</span></p>
        <button id="upgrade-button">Upgrade (50 cookies)</button>
        <button id="buy-button">Buy Worker (100 cookies)</button>
    </div>
</div>

<script>
    let cookieCount = 0;
    let workers = 0;
    let cookiePerClick = 100;
    let upgradeCost = 50;
    let buyCost = 100;

    // Get elements
    const cookieDisplay = document.getElementById('cookie-count');
    const workerDisplay = document.getElementById('worker-count');
    const cookie = document.getElementById('cookie');
    const upgradeButton = document.getElementById('upgrade-button');
    const buyButton = document.getElementById('buy-button');

    // Cookie click function
    cookie.addEventListener('click', function() {
        cookieCount += cookiePerClick;
        updateDisplay();
    });

    // Upgrade function
    upgradeButton.addEventListener('click', function() {
        if (cookieCount >= upgradeCost) {
            cookieCount -= upgradeCost;
            cookiePerClick += 1; // Increase cookies per click
            upgradeCost = Math.floor(upgradeCost * 1.5); // Increase the cost for the next upgrade
            updateDisplay();
            upgradeButton.textContent = `Upgrade (Next: ${upgradeCost} cookies)`;
        } else {
            alert('Not enough cookies!');
        }
    });

    // Buy workers function
    buyButton.addEventListener('click', function() {
        if (cookieCount >= buyCost) {
            cookieCount -= buyCost;
            workers++;
            updateDisplay();
            buyButton.textContent = `Buy Worker (Next: ${buyCost} cookies)`;
        } else {
            alert('Not enough cookies!');
        }
    });

    // Update the display
    function updateDisplay() {
        cookieDisplay.textContent = cookieCount;
        workerDisplay.textContent = workerCount;

        if (cookieCount >= upgradeCost) {
            upgradeButton.disabled = false;
        } else {
            upgradeButton.disabled = true;
        }

        if (cookieCount >= buyCost) {
            buyButton.disabled = false;
        } else {
            buyButton.disabled = true;
        }
    }
</script>
