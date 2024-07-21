---
layout: page
title: Zeitverschiebung
subtitle: Aktuelle Uhrzeit in Braunschweig und Omaha
---

Auf dieser Seite werden die aktuellen Uhrzeiten in Braunschweig und Omaha angegeben. Vielleicht hilft diese Information ja bei der Kontaktaufnahme 😄


<html>
<style>
    #clocks {
        text-align: center;
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
        font-size: x-large;
        text-align: center;
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
    .clock h2 {
        margin-top: 0;
        margin-bottom: 5px;
    }
</style>
<body>
<center>
<div id="clocks">
    <div id="berlin" class="clock">
        <h2>Berlin</h2>
        <div id="berlinTime"></div>
        <div id="berlinDate"></div>
    </div>
    <div id="omaha" class="clock">
        <h2>Omaha</h2>
        <div id="omahaTime"></div>
        <div id="omahaDate"></div>
    </div>
    <div id="newYork" class="clock">
        <h2>New York</h2>
        <div id="newYorkTime"></div>
        <div id="newYorkDate"></div>
    </div>
</div>

<script>
function updateClocks() {
    const berlinTime = new Date().toLocaleTimeString("de", {timeZone: "Europe/Berlin", hour: "numeric", minute: "2-digit"});
    document.getElementById("berlinTime").textContent = berlinTime;

    const berlinDate = new Date().toLocaleDateString("de", {timeZone: "Europe/Berlin", month: "long", day: "2-digit", year: "numeric"});
    document.getElementById("berlinDate").textContent = berlinDate;

    const chicagoTime = new Date().toLocaleString("de", {timeZone: "America/Chicago", hour: "numeric", minute: "2-digit"});
    document.getElementById("omahaTime").textContent = chicagoTime;

    const chicagoDate = new Date().toLocaleString("de", {timeZone: "America/Chicago", month: "long", day: "2-digit", year: "numeric"});
    document.getElementById("chicagoDate").textContent = chicagoDate;

    const newYorkTime = new Date().toLocaleString("de", {timeZone: "America/New_York", hour: "numeric", minute: "2-digit"});
    document.getElementById("newYorkTime").textContent = newYorkTime;

    const newYorkDate = new Date().toLocaleString("de", {timeZone: "America/New_York", month: "long", day: "2-digit", year: "numeric"});
    document.getElementById("newYorkDate").textContent = newYorkDate;
}

// Update clocks every second
setInterval(updateClocks, 1000);

// Initial update
updateClocks();
</script>
</center>
</body>
</html>