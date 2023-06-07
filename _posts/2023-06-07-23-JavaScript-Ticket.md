---
layout: post
title: JavaScript Ticket 
---

<html>
<head>
    <title>Click the Circles</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
        }
        #game-container {
            width: 400px;
            height: 400px;
            position: relative;
        }
        .circle {
            width: 80px;
            height: 80px;
            background-color: #ff4081;
            border-radius: 50%;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            font-weight: bold;
            font-size: 24px;
            transition: background-color 0.2s;
        }
        .circle:hover {
            background-color: #ff6699;
        }
    </style>
</head>
<body>
    <h1>Click the Circles</h1>
    <div id="game-container"></div>
    <script>
        function startGame() {
            const gameContainer = document.getElementById('game-container');
            const circles = [];
            let score = 0;
            function createCircle() {
                const circle = document.createElement('div');
                circle.classList.add('circle');
                circle.addEventListener('click', removeCircle);
                circle.innerText = getRandomNumber(1, 10);
                gameContainer.appendChild(circle);
                circles.push(circle);
            }
            function removeCircle() {
                const index = circles.indexOf(this);
                if (index > -1) {
                    circles.splice(index, 1);
                }
                gameContainer.removeChild(this);
                score++;
                updateScore();
            }
            function updateScore() {
                document.getElementById('score').innerText = score;
            }
            function getRandomNumber(min, max) {
                return Math.floor(Math.random() * (max - min + 1)) + min;
            }
            setInterval(createCircle, 1000);
        }
        startGame();
    </script>
    <h2>Score: <span id="score">0</span></h2>
</body>
</html>
