# Project Plan

## Guidance steps provided by The Odin Project

1. Your calculator is going to contain functions for all of the basic math operators you typically find on calculators, so start by creating functions for the following items: (add, subtract, multiply, divide)

2. A calculator operation will consist of a number, an operator, and another number. For example, 3 + 5. Create three variables for each of the parts of a calculator operation. Create a variable for the first number, the operator, and the second number. You’ll use these variables to update your display later.

3. Create a new function 'operate' that takes an operator and 2 numbers and then calls one of the above functions on the numbers

4. Create a basic HTML calculator with buttons for each digit, each of the above functions and an “Equals” key. There should also be a display for the calculator and a 'clear' button. Do not worry about wiring up the JS just yet.

5. Create the functions that populate the display when you click the number buttons. You should be storing the ‘display value’ in a variable somewhere for use in the next step.

6. Make the calculator work! You’ll need to store the first number and second number that are input into the calculator, utilize the operator that the user selects, and then operate() on the two numbers when the user presses the “=” key. You should already have the code that can populate the display, so once operate() has been called, update the display with the ‘solution’ to the operation. This is the hardest part of the project. You need to figure out how to store all the values and call the operate function with them. Don’t feel bad if it takes you a while to figure out the logic.

7. Extras: 
    - Your calculator should not evaluate more than a single pair of numbers at a time. Example: you press a number button (12), followed by an operator button (+), a second number button (7), and finally a second operator button (-). Your calculator should then do the following: first, evaluate the first pair of numbers (12 + 7), second, display the result of that calculation (19), and finally, use that result (19) as the first number in your new calculation, along with the next operator (-).
    - You should round answers with long decimals so that they don’t overflow the screen
    - Pressing “clear” should wipe out any existing data. Make sure the user is really starting fresh after pressing “clear”
    - Display a snarky error message if the user tries to divide by 0… and don’t let it crash your calculator!

## My rewording of the project for adhanced understanding

Start by creating functions for add, subtract, multiply and divide.

We define a operation that we calculate by 2 operands and an operator, each stored in their own variables

Create a function called 'operate' taking these 3 variables as parameters, which calls a operation function on them

Using only HTML, create a calculator that has every digit, every operation that we made a function for, a clear button, an equals button and a display.

Create functions that put numbers on the screen of the display when you click buttons on the calculator. The value that is displayed should have its own variable

Make variables for the first and second number you add into the calculator, and using the one of the operations that user chooses, run operate() when they click '=', and update the calculator display with the result

Make sure that your calculator doesn't evaluate more than a pair of numbers at one time
Make sure numbers with very large decimals are restricted in size to fit the display
Generate an error for the case where the user tries to divide by 0, so it doesn't stop the calculator from working

