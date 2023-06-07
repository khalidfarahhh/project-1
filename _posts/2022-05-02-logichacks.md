---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Logic Hacks
---

<!DOCTYPE html>
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




# logic gates 
1. Logic gates can be used to execute basic computer functions by implementing Boolean logic operations on binary inputs, which can be used to perform arithmetic, comparison, and control operations in a computer’s central processing unit (CPU) and other digital circuits.
2. Boolean operations are abstract mathematical operations defined in Boolean algebra, while logic gates are physical devices or circuits that implement these operations by controlling the flow of electricity through them. Boolean operations are the abstract concepts used to describe logical relationships between variables, while logic gates are the physical components that perform these operations in digital circuits.
3. I wasnt locked in got 2 wrong

![]({{site.baseurl}}/images/Screenshot 2023-05-02 130749.png)

# Binary Logic 
![]({{site.baseurl}}/images/Screenshot 2023-05-02 130900.png)

# Binary Math 
1. Write the two numbers one above the other, with the second number (the subtrahend) below the first number (the minuend). Starting from the rightmost digit of the subtrahend, subtract each digit from the corresponding digit of the minuend. If the digit in the subtrahend is larger than the digit in the minuend, borrow 1 from the next digit to the left in the minuend. Write the result of each subtraction below the corresponding digits of the subtrahend. If any borrow occurs in step 2, the borrowed digit in the minuend is reduced by 1. This process is repeated until no borrow occurs. Write the result of the subtraction as a binary number.
2. My fetch code 

![]({{site.baseurl}}/images/Screenshot 2023-05-02 131905.png)

# Api hacks 
![]({{site.baseurl}}/images/Screenshot 2023-05-02 131619.png)
![]({{site.baseurl}}/images/Screenshot 2023-05-02 131641.png)

# Git hub hacks 
Netlify is a hosting service that offers a number of features that set it apart from other hosting services. One major advantage of Netlify is that it provides a simple and intuitive platform for building, deploying, and managing modern web projects.
