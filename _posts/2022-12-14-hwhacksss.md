---
toc: true
layout: post
badges: true
comments: true
author: Khalid farah
categories: [fastpages, markdown]
title: Lesson 12-13 hacks
---

3.12 Part 1
Problem 1: This problem involves parameters Qais is writing code to calculate formulas from his math class. He's currently working on a procedure to calculate average speed, based on this formula:
Average speed=

Total Time/Total Distance​

Highlight which of these is the best procedure for calculating and displaying average speed. PROCEDURE calcAvgSpeed (distance, time) { DISPLAY (distance/time) } PROCEDURE calcAvgSpeed (distance) { DISPLAY (distance/time) } PROCEDURE calcAvgSpeed (distance, time) { DISPLAY (time/distance) }

Problem 2: Procedures with return values James Hunter is looking through his classmate's program and sees a procedure called heightenEmotions:
PROCEDURE heightenEmotions(myEmotion){ moreEnergy ← CONCAT(myEmotion, "!!!") moreVolume ← UPPER(moreEnergy)

RETURN moreVolume }

That procedure manipulates strings using two built-in procedures, CONCAT for concatenating two strings together, and UPPER for converting a string to uppercase.

James Hunter then sees this line of code:

heightenEmotions("im mad")

After that line of code runs, will nothing be displayed?

True, because it does not have DISPLAY in the procedure

False

Problem 3: Procedures with return values Bubz is writing a program to calculate the carbon footprint of his activities. The procedure calcFlightFootprint calculates the pounds of carbon dioxide produced per passenger in a flight that covers a given number of miles and seats a given number of passengers.
PROCEDURE calcFlightFootprint(numMiles, numPassengers) {

CO2_PER_MILE ← 53.29

carbonPerFlight ← numMiles * CO2_PER_MILE

carbonPerPassenger ← carbonPerFlight / numPassengers

RETURN carbonPerPassenger

}

Bubz wants to use that procedure to calculate the total footprint for his two upcoming flights: LA to NY: 2,451 miles and 118 passengers NY to London: 3,442 miles and 252 passengers

Which of these code snippets successfully calculates and stores her total footprint? Highlight 2 answers.

totalFootprint ← calcFlightFootprint(2451, 118) + calcFlightFootprint(3442, 252)

totalFootprint ← calcFlightFootprint(2451, 118 + 3442, 252)

totalFootprint ← calcFlightFootprint((2451, 118) + (3442, 252))

laNyCarbon ← calcFlightFootprint(2451, 118) nyLondonCarbon ← calcFlightFootprint(3442, 252) totalFootprint ← laNyCarbon + nyLondonCarbon

3.12 Part 2
What is a?
a -- ?
b -- ?
c -- 9
PROCEDURE find a () { b <-- 9 9
a <-- b c
Print (a) }

Answer: a is 9

What is the cost?
cost ⟵ 173 tax - 10% PROCEDURE applytax (cost, percentDiscounted){

temp <-- 100 + percentTaxed
temp <-- temp / 100
cost <-- cost x temp
Print(cost)}
Answer: The cost $190.30

What is the celsius value?
Temperature - 103 Degrees
PROCEDURE convert Fahrenheit (temperature) {
Celsius <-- temperature - 32
Celsius <-- Celsius x 5/9
Print (Celsius)}

Answer: 39.4 Celsius

3.13 Parts 1 and 2
Create a procedure that is meant to replace the top running backs yards per game in one season if the current running back has more yards per game
Necessary Parameters: toprbyardspg(100), currentrbyards(1260), totalGames(12)
PROCEDURE replaceTopRb(toprbyardspg(100), curerntrbyards(1260), totalgames){
If (currentRbYards(1260) > toprbyardspg(100)){
toprbyardspg <-- currentRbYards
}
}
Write a procedure that will allow the A+ to get to the 1, while avoiding the black boxes.

PROCEDURE getAplus(){
If (can_MoveForward):
Move_Forward
Else (can_MoveRight):
Rotate_Right
Move_Forward
If (can_MoveLeft);
Rotate_Left
Move_forward
}
Which Is the Correct Way to define the Name of a Procedure?

A. PROCEDURE MYLIST
B. PROCEDURE MyList
C. procedure mylist

Answer: B. because procedure should be in all capitals and part of the the declared procedure should be capitalized, not all and not none.

Write A Procedure that gets the Santa to the Christmas Tree
PROCEDURE SantaToTree{ count = 0
Move_Forward
Rotate_Left
Move_Forward( until count = 6)
break
Rotate_Left
Move_Forward }
What I have learned:
I learned the basics in creating a procedure:
that the name needs to be simple but make sense
that you can use for and while loops and iteration to shorten the code
Procedure in the code should be written in all caps like "PROCEDURE"
In algorithms:
there are many different algorithms to reach a certain solution
you can also use for and while loops and iteration to shorten algorithms