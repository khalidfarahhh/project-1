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
            function createCircle() {
                const circle = document.createElement('div');
                circle.classList.add('circle');
                circle.addEventListener('click', removeCircle);
                gameContainer.appendChild(circle);
                circles.push(circle);
            }
            function removeCircle() {
                const index = circles.indexOf(this);
                if (index > -1) {
                    circles.splice(index, 1);
                }
                gameContainer.removeChild(this);
            }
            setInterval(createCircle, 1000);
        }
        startGame();
    </script>
</body>
</html>
