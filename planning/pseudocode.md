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


