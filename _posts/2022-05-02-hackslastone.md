---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Tinisha hacks 
---

1. 
- Give an example of iteration.
search algorithm finds certain element in a list
- What is the difference between a for loop and while loop? That is, when would you use a for loop and when would you use a while loop?
use for loop when repeating a certain number of times, and while loop to repeat until condition is met
- In the APCSP AP exam, what number do indexes start with? important to know
1
- Are dictionaries and lists mutable?
ordered dictioanries are not

2. list 
Lists are forms of abstraction, used to store large sums of data

3. Iteration 
Iterative statements are also called loops, and they repeat themselves over and over until the condition for stopping is met.

4. Describe the difference between a "REPEAT n TIMES" loop VS a "REPEAT UNTIL (condition)" loop. it is important you know this for the AP Exam
one repeat a certain amount of times, the other repeats until a condition is met.

5. 
What are some libraries that we've learned about? What are their advantages/disadvantages?
Numpy, Matlib, Yfinance, these libraries provide data and procedures for the user.

6. an unordered collection of key-value pairs, where each key is known and associated with a specific value

7. 
Compare and contrast lists and dictionaries.
- Lists are numbered based on the index, dictionaries have keys and values
Do dictionary keys need to be unique?
- yes, otherwise you could not access certain keys
8. List comprehension is similar to iteration in that both involve the process of looping over a sequence of values and performing some operation on each value.
# CODE 
users = [    {'name': 'Ava', 'age': 28, 'hobby': 'reading'},    {'name': 'Ben', 'age': 35, 'hobby': 'painting'},    {'name': 'Charlotte', 'age': 22, 'hobby': 'gaming'},    {'name': 'David', 'age': 45, 'hobby': 'cooking'},    {'name': 'Emily', 'age': 19, 'hobby': 'swimming'},    {'name': 'Frank', 'age': 31, 'hobby': 'gardening'},    {'name': 'Grace', 'age': 26, 'hobby': 'photography'},    {'name': 'Henry', 'age': 40, 'hobby': 'traveling'},    {'name': 'Isaac', 'age': 27, 'hobby': 'music'},    {'name': 'Julia', 'age': 23, 'hobby': 'dancing'}]

def get_user(name):
    for user in users:
        if user['name'] == name:
            print(user)
            print()

            
def get_users():
    for user in users:
        print("Name:", user['name'])
        print("Age:", user['age'])
        print("Hobby:", user['hobby'])
        print()

get_user('Ben')
get_users()

# SIMULATION 
- simulates population of dudes in 100 years 
import random

population = [100] # start with 100 dudes
num_years = 10

for year in range(1, num_years+1):
    new_dudes = population[year - 1] # get the number of dudes from last year
    # add some randomness to the new dude production
    new_dudes *= random.uniform(1.01, 1.03) # assume 1-3% annual growth
    population.append(round(new_dudes)) # add the new dudes to the list

print(population)
