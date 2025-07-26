<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<title>Tovar Score Center</title>

<style>

    body {

        margin: 0;

        background: #111;

        font-family: Arial, sans-serif;

        color: #fff;

        overflow-x: hidden;

    }

    header {

        text-align: center;

        padding: 20px;

        font-size: 2.5em;

        color: #FFD700;

        text-shadow: 0 0 15px #FF4500;

    }

    .scoreboard {

        display: flex;

        justify-content: space-around;

        padding: 20px;

        animation: glow 8s infinite alternate;

    }

    @keyframes glow {

        0% { box-shadow: 0 0 20px #FF0000; }

        50% { box-shadow: 0 0 40px #00FFAA; }

        100% { box-shadow: 0 0 20px #FFD700; }

    }

    .column {

        flex: 1;

        background: rgba(0,0,0,0.85);

        margin: 10px;

        padding: 15px;

        border-radius: 12px;

        box-shadow: 0 0 15px #FFD700;

    }

    .column h2 {

        text-align: center;

        font-size: 2em;

        color: #FFD700;

        margin-bottom: 15px;

    }

    .game {

        margin: 15px 0;

        padding: 10px;

        background: rgba(50,50,50,0.8);

        border-radius: 8px;

        text-align: center;

    }

    .team {

        font-size: 1.5em;

    }

    .score {

        font-size: 2.5em;

        font-weight: bold;

        display: block;

        margin: 5px 0;

    }

    .status {

        font-size: 1em;

        margin-top: 5px;

        padding: 3px 8px;

        border-radius: 5px;

        display: inline-block;

    }

    .live { background: red; }

    .final { background: green; }

    .upcoming { background: blue; }

    footer {

        text-align: center;

        margin: 20px 0;

        color: #ccc;

        font-size: 1.2em;

    }

</style>

</head>

<body>

<header>

    Tovar Score Center<br>

    <span id="clock"></span>

</header>



<div class="scoreboard">

    <div class="column">

        <h2>NFL</h2>

        <div class="game">

            <div class="team">49ers (10-3)</div>

            <div class="score">28</div>

            <div class="team">Cowboys (9-4)</div>

            <div class="score">21</div>

            <div class="status live">LIVE</div>

        </div>

        <div class="game">

            <div class="team">Chiefs (8-5)</div>

            <div class="score">14</div>

            <div class="team">Bills (10-2)</div>

            <div class="score">24</div>

            <div class="status final">FINAL</div>

        </div>

    </div>



    <div class="column">

        <h2>MLB</h2>

        <div class="game">

            <div class="team">Yankees (50-30)</div>

            <div class="score">3</div>

            <div class="team">Red Sox (45-35)</div>

            <div class="score">5</div>

            <div class="status live">LIVE</div>

        </div>

        <div class="game">

            <div class="team">Dodgers (60-25)</div>

            <div class="score">2</div>

            <div class="team">Giants (40-45)</div>

            <div class="score">6</div>

            <div class="status final">FINAL</div>

        </div>

    </div>



    <div class="column">

        <h2>NCAA Top 25</h2>

        <div class="game">

            <div class="team">Alabama (11-1)</div>

            <div class="score">28</div>

            <div class="team">Georgia (12-0)</div>

            <div class="score">31</div>

            <div class="status live">LIVE</div>

        </div>

        <div class="game">

            <div class="team">Ohio State (10-2)</div>

            <div class="score">17</div>

            <div class="team">Michigan (12-0)</div>

            <div class="score">24</div>

            <div class="status upcoming">UPCOMING</div>

        </div>

    </div>

</div>



<footer>

    Last Updated: <span id="updated"></span><br>

    Created by Tovar Score Center

</footer>



<script>

function updateClock() {

    const now = new Date();

    document.getElementById('clock').innerText = now.toLocaleString();

    document.getElementById('updated').innerText = now.toLocaleTimeString();

}

setInterval(updateClock, 1000);

updateClock();

</script>



</body>

</html>
