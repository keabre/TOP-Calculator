# PSEUDOCODE

## Rough steps through the program lifecycle

- FROM START

- user will have the option to click a number

    - if the user clicks clear, '=', or an operation, nothing will happen

    - if the user clicks a number, display it to the screen and save it in a variable

        - if the number clicked is 0, then nothing happens, and the program goes back to waiting for the user to click a number

- after successfully clicking a digit, the user will have the option to click another digit, clear or an operator

    - if the user clicks another digit, it is added accordingly to the previous number to create a new number, stores the combination of these digits as a new number in the variable the first number is stored in, and the value of this variable is displayed on the screen in place of the previous number and the program goes back to waiting for the user to click another digit, clear or an operator 

    - if the user clicks 'clear', the first number is removed from the display and the first number variable is cleared, the display shows a blank screen again and the program goes back to the step where the program waits for the user to enter a number

    - if the user clicks an operator, this clicked operator is shown on the screen after the first number and the operator is stored in a variable for this calculation 

    - if the user clicks '=', nothing happens, and the program returns to waiting for the user to click another digit, clear or an operator

- after sucessfully clicking an operator, the user will have the option to click a second number

    - if the user clicks a second number, this number is displayed on the screen after the operator and is stored in a variable for the second operand

        - if the second number that the user enters is a 0, nothing happens but the program will warn the user that division by 0 is not allowed, the program will go back to waiting for the user to click a second number

    - if the user clicks '=', then nothing happens, and the program returns to waiting for the user to click a second digit

    - if the user clicks 'clear', then the display is cleaned and shows nothing, the variables for the first operand and the operator are returned to their default values and the program goes back to waiting for the first number to be entered

    - if the user clicks an operator, then nothing happens, and the program returns to waiting for the user to click a second digit

- after sucessfully clicking a second number, the user will have the option to click another number, clear or press '='

    - if the user clicks another number, this number is added to the previous number to create a new number, stores the combination of these digits as a new number in the variable for the second operand where the previous number was stored in, and the value of this variable is displayed on the screen in place of the previous number and the program goes back to waiting for the user to click another number, clear, or press '='

    - if the user clicks another operator, then nothing happens, and the program returns to waiting for the user to click another number, clear, or press '='
    
    - if the user clicks 'clear', then the display is cleaned and shows nothing, the variables for the first and second operand, and the operator are returned to their default values and the program goes back to waiting for the first number to be entered

    - if the user clicks '=', then the operate() function runs, using the values in the variables for the two operands, and the calulation function ran will depend on what operator is stored in the operator variable. The return value of the function (which will be the result of the calculation), will be stored in a variable for the calculation result and will be displayed on the screen in place of everything currently there. The program will then go back to waiting for the user to click another digit, clear or an operator, except this time around the program will not allow the user to enter another digit as the value has already been determined from the last calculation, so the user will only be able to press the clear button or an operator button.

- TO END

## Pseudocode

### Gather DOM Elements

Select all buttons with the class of 'digit' and save them in a variable called digitButtons

Select all buttons with the class of 'operator' and save them in a variable called operatorButtons

Select the button with the id of 'clear' and save it in a variable called clearButton

Select the button with the id of 'equals' and save it in a variable called equalsButton

Select the div with the id of 'calc-display' and save it in a variable called calculatorDisplay

### Define operator functions

- Divide

Create a function called 'divide' that takes two arguments, denoted by the parameters 'operandOne' and 'operandTwo'

Inside the function:

return the result of operandOne divided by operandTwo

- Multiply

Create a function called 'multiply' that accepts two arguments, denoted by the parameters 'operandOne' and 'operandTwo'

Inside the function

return the result of operandOne multiplied by operandTwo

- Add

Create a function called 'add' that accepts two arguments, denoted by the parameters 'operandOne' and 'operandTwo'

Inside the function:

return the result of operandOne added to operandTwo

- Subtract

Create a function called 'subtract' that accepts two arguments, denoted by the parameters 'operandOne' and 'operandTwo'

Inside the function: 

return the result of operandOne subtracted by operandTwo

### Define temporary variables

Create a variable to hold the first operand of the current calculation called currentFirstOperand, set this variable to 0 as default
At any time there is a value in the variable calculationResult, set currentFirstOperand to calculationResult

Create a variable to hold the operator of the current calculation called currentOperator, set this variable to and empty string as default

Create a variable to hold the second operand of the current calculation called currentSecondOperand, set this variable to 0 as default

Create a variable to hold the result of the calculation after the user clicks the '=' button called calculationResult, set this variable to 0 as default

Create a variable for the display value of the current calculation called currentDisplayValue, set this variable to an empty string as default

### Define function to determine which calculation function to utilise

Create a function called 'operate' that accepts three arguments, denoted by the parameters, operandOne, operandTwo, and operator

Inside the function: 

if the operator argument is 'divide'
then run the divide function, passing it the arguments operandOne and operandTwo
set calculationResult to the return value of the divide function
run the function updateDisplay, passing in the argument 'CALCULATE'

if the operator argument is 'multiply'
then run the multiply function, passing it the arguments operandOne and operandTwo
set calculationResult to the return value of the multiply function
run the function updateDisplay, passing in the argument 'CALCULATE'

if the operator argument is 'add'
then run the add function, passing it the arguments operandOne and operandTwo
set calculationResult to the return value of the add function
run the function updateDisplay, passing in the argument 'CALCULATE'

if the operator argument is 'subtract'
then run the subtract function, passing it the arguments operandOne and operandTwo
set calculationResult to the return value of the subtract function
run the function updateDisplay, passing in the argument 'CALCULATE'

### Define function that populates the display when user clicks buttons

Create a function called 'updateDisplay' that accepts an argument as a string, denoted by the parameter 'selection', that allows the program to determine which code to run in this function

- if currentFirstOperand is 0, and if currentOperator is an empty string, and if currentSecondOperator is 0 (default states), then:

do not change the value of currentDisplayValue, keep the value as an empty string
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

- if currentFirstOperand is not 0, currentOperator is an empty string, and if currentSecondOperator is 0, then:

change the value of currentDisplayValue to the value of currentFirstOperand, with an empty space following the number
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

- if currentFirstOperand is not 0, and currentOperator is not an empty string, and if currentSecondOperator is 0, then:

change the value of currentDisplayValue to the value of currentFirstOperand and the value of currentOperator, with a space between the two
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

- if currentFirstOperand is not 0, and currentOperator is not an empty string, and if currentSecondOperator is not 0, then:

change the value of currentDisplayValue to the value of currentFirstOperand, currentOperator and currentSecondOperand, all with a space between
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

- if currentFirstOperand is not 0, and currentOperator is not an empty string, and if currentSecondOperator is not 0 and the argument selection is 'CALCULATE', then:

change the value of currentDisplayValue to currentFirstOperand with a space in front of it, assuming the program correctly sets currentFirstOperand to calculationResult
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

- if the argument selection is 'CLEAR', then: 

set the value of currentDisplayValue as an empty string
change the value of the DOM container variable calculatorDisplay to currentDisplayValue

### Define function for when the user clicks the clear button

Create a function called 'clearDisplay' that takes no arguments

Inside the function:

set currentFirstOperand to a value of 0

set currentOperator to a value of an empty string

set currentSecondOperand to a value of 0

set calculationResult to a value of 0

set currentDisplayValue to a value of an empty string

run the updateDisplay function to clear the calculator display, passing in the argument 'CLEAR'
