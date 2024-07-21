---
layout: page
title: Zeitverschiebung
subtitle: Aktuelle Uhrzeit in Braunschweig und Omaha
---

Auf dieser Seite werden die aktuellen Uhrzeiten in Braunschweig und Omaha angegeben. Vielleicht hilft diese Information ja bei der Kontaktaufnahme 😄


<html>
<style>
    h1 {
        margin-top: 20px;
    }
    #clocks {
        font-size: x-large;
        display: inline-flex;
        flex-direction: row;
        align-items: center;
        margin-top: 15px;
        margin-bottom: 15px;
        margin-left: 15px;
        margin-right: 15px;
    }
    .clock {
        border: 2px solid #333;
        border-radius: 10px;
        padding: 15px;
        /*width: calc(100% - 40px); /* Adjusting box size */
        max-width: 400px;
        margin-top: 10px;
        margin-bottom: 10px;
        margin-left: 10px;
        margin-right: 10px;
    }
    .clock h3 {
        margin-top: 0;
        margin-bottom: 5px;
    }
</style>
<body>
<div id="clocks">
    <div id="berlin" class="clock">
        <h3>Berlin</h3>
        <div id="berlinTime"></div>
    </div>
    <div id="Omaha" class="clock">
        <h3>Omaha</h3>
        <div id="omahaTime"></div>
    </div>
    <div id="newYork" class="clock">
        <h3>New York</h3>
        <div id="newYorkTime"></div>
    </div>
</div>

<script>
function updateClocks() {
    const londonTime = new Date().toLocaleString("de", {timeZone: "Europe/Berlin"}).slice(0, -3);
    document.getElementById("berlinTime").textContent = londonTime;

    const newDelhiTime = new Date().toLocaleString("de", {timeZone: "America/Chicago"}).slice(0, -3);
    document.getElementById("omahaTime").textContent = newDelhiTime;

    const newYorkTime = new Date().toLocaleString("de", {timeZone: "America/New_York"}).slice(0, -3);
    document.getElementById("newYorkTime").textContent = newYorkTime;
}

// Update clocks every second
setInterval(updateClocks, 1000);

// Initial update
updateClocks();
</script>
</body>
</html>