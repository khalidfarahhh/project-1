---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Logic Hacks
---

<html>
<head>
    <title>Fruit Ninja</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
#game-container {
            width: 100%;
            height: 100vh;
            background-color: #f1f1f1;
            position: relative;
            cursor: none;
        }
.fruit {
            width: 100px;
            height: 100px;
            background-image: url('fruit.png');
            background-size: cover;
            position: absolute;
            top: 0;
            left: 0;
            cursor: pointer;
            transition: top 2s cubic-bezier(0.45, 0, 0.55, 1), transform 1s ease-in-out;
        }
    </style>
</head>
<body>
    <h1>Fruit Ninja</h1>
    <div id="game-container"></div>
<script>
        function startGame() {
            const gameContainer = document.getElementById('game-container');
            const fruits = ['apple', 'banana', 'grape', 'orange', 'watermelon'];
function getRandomPosition(max) {
                return Math.floor(Math.random() * max);
            }
function createFruit() {
                const fruit = document.createElement('div');
                const randomFruit = fruits[Math.floor(Math.random() * fruits.length)];
                fruit.classList.add('fruit', randomFruit);
                fruit.style.top = getRandomPosition(gameContainer.offsetHeight - 100) + 'px';
                fruit.style.left = getRandomPosition(gameContainer.offsetWidth - 100) + 'px';
                fruit.addEventListener('click', sliceFruit);
                gameContainer.appendChild(fruit);
setTimeout(() => {
                    fruit.style.top = '100%';
                    fruit.style.transform = 'translate(-50%, -50%) rotate(180deg)';
                }, 1000);
            }
function sliceFruit() {
                this.classList.add('sliced');
                setTimeout(() => {
                    gameContainer.removeChild(this);
                }, 1000);
            }
setInterval(createFruit, 1500);
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
