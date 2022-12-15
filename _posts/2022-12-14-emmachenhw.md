---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Leesson 14-14 hacks
---

# Reflection
- I learned about documentation, libraries, and APIs. Documentation is a part of the AP Exam project part and it requires explaining what and how your code works. Libraries help make your coding experience more efficient because they are pre-written and you can reference them throughout your code. I researched one library that utilizes Python: numPy, which works with arrays.


# Multiple Choice
B) a random integer between 'a' and 'b' inclusive
A) x = start, y = stop, z = step
A) random.item() does not exist
# Short Answer
Libraries are convenient because they provide procedures and prewritten code to maximize the efficiency of programmers
This procedure takes a list of strings and returns who will buy the meal today
import random 

 takes user input, puts it into a list of names
names_string = input("Give me everybody's names, seperated by a comma.")
names = names_string.split(",")

num_items = len(names)

 uses random to choose a random number
random_choice = random.randint(0, num_items - 1)

  associates random number with a name
person_who_will_pay = names[random_choice]

 prints name
print(f"{person_who_will_pay} is going to buy the meal today!")
# Coding challenges
import random
NAMES = ["Aiden", "Brayden", "Bradley", "Harambe", "Charles", "BigChungus", "Chad", "Brett", "Dorian", "Ryan", "Varalu", "Rohin", "Advay", "SmallChungus"]
rand_list = []

def randomPeople(names, new_names):
    count = 1
    while count <= 5:
        number = random.randint(0, len(names) - 1)
        new_names.append(names[number])
        count += 1
    return new_names

print(randomPeople(NAMES, rand_list))
['Charles', 'BigChungus', 'Rohin', 'Dorian', 'Aiden']
import random
score1 = 0
score2 = 0

def greatestRoll():
    score1 = random.randint(1, 6) + random.randint(1, 6)
    score2 = random.randint(1, 6) + random.randint(1, 6)
    if score1 > score2:
        print("Player 1 won with a score of " + str(score1) + " points!")
    if score1 < score2:
        print("Player 2 won with a score of " + str(score2) + " points!")
    if score1 == score2:
        print("Both players tied with " + str(score1) + " points!")

greatestRoll()
Player 1 won with a score of 9 points!
