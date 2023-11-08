# Avanced-Scientific-Calculator
I am Using to make the Scientific Calculator Using [ Html Css and javscript ]
HTML ELEMENTS :
inputElement: Represents the input field where the user enters numbers and expressions.
outputOperationElement: Displays the current operation being performed (e.g., +, -, *, /).
outputResultElement: Displays the calculated result of the expression.
Mode Switching:

SCIENTIFIC_MODE: A boolean flag indicating whether the calculator is in scientific mode.
scientificMode: The button element for switching to scientific mode.
normalMode: The button element for switching to normal mode.
Event Handling:

scientificMode.addEventListener("click", ...): Handles the click event on the scientificMode button.

Sets SCIENTIFIC_MODE to true.
Adds the "active-calc" class to the scientificMode button, indicating the active mode.
Removes the "active-calc" class from the normalMode button.
Calls disableAdvaceKey() to disable advanced keys in normal mode.
normalMode.addEventListener("click", ...): Handles the click event on the normalMode button.

Sets SCIENTIFIC_MODE to false.
Removes the "active-calc" class from the scientificMode button.
Adds the "active-calc" class to the normalMode button, indicating the active mode.
Calls disableAdvaceKey() to disable advanced keys in normal mode.
Data Storage:

data: An object to store the current operation and formula.
operation: An array of arithmetic operations (+, -, *, /).
formula: An array of numbers and expressions.
Calculation Variables:

OPERATIONS: An array of basic arithmetic operations (+, -, *, /).

POWER: A string representing the power operation (POWER()).

FACTORIAL: A string representing the factorial operation (FACTORIAL()).

CUBE: A string representing the cube operation (CUBE()).

ans: A variable to store the calculated result.


Math functions: These buttons represent mathematical operations like cube, cube root, x-inverse, square, square root, factorial, log, ln, power, and exponential (exp).

Trigo functions: These buttons represent trigonometric functions like cosine (cos), sine (sin), tangent (tan), inverse cosine (acos), inverse sine (asin), and inverse tangent (atan).

Number buttons: These buttons represent numerical values from 0 to 9, including the decimal point (comma) and pi (π).

Operator buttons: These buttons represent basic arithmetic operators like addition (+), subtraction (-), multiplication (×), and division (÷).

Key buttons: These buttons represent special keys like clear (C), delete (⌫), degree (deg), radian (rad), and equals (=).

Constant buttons: These buttons represent mathematical constants like e (e) and the answer from the previous calculation (ANS).


The first line declares a variable RADIAN and assigns it a value of true.
The next two lines select two HTML elements with the IDs rad and deg and assign them to the variables radBtn and degBtn, respectively.
The fourth line adds the class active-angle to the radBtn element.
The angleToggler() function is defined on the next line. This function toggles the active-angle class on both radBtn and degBtn elements.
The inputElement element is selected and an event listener is added to it on the next line. When the element is clicked, the function passed as the second argument is called.
The calculator() function is defined on the next line. This function takes a button object as its argument and performs different actions based on the type property of the object.


The first line declares a variable RADIAN and assigns it a value of true.

The next two lines select two HTML elements with the IDs rad and deg and assign them to the variables radBtn and degBtn, respectively.

The fourth line adds the class active-angle to the radBtn element.

The angleToggler() function is defined on the next line. This function toggles the active-angle class on both radBtn and degBtn elements.

The inputElement element is selected and an event listener is added to it on the next line. When the element is clicked, the function passed as the second argument is called.

The calculator() function is defined on the next line. This function takes a button object as its argument and performs different actions based on the type property of the object.

If the type is "operator" or "number", the function pushes the symbol and formula properties of the button object to the operation and formula arrays, respectively.
If the type is "trigo_function", the function pushes the symbol property of the button object followed by an opening parenthesis to the operation array, and the formula property of the button object followed by an opening parenthesis to the formula array.
If the type is "math_function", the function performs different actions based on the name property of the button object. For example, if the name is "power", the function pushes the string "^(" to the operation array and the formula property of the button object to the formula array.
If the type is "key", the function performs different actions based on the name property of the button object. For example, if the name is "clear", the function clears the operation and formula arrays and updates the output result to 0.

The eval() function is used to evaluate a mathematical expression string.
The try-catch block is used to catch any syntax errors that may occur during the evaluation of the expression.
If a syntax error occurs, the code sets the result to “Syntax Error!” and returns it.
The powerBaseGetter() function extracts the base of each power operation in the expression string.
The factorialNumGetter() function extracts the number being factorialized in each factorial operation in the expression string.

The eval() function is used to evaluate a mathematical expression string.
The try-catch block is used to catch any syntax errors that may occur during the evaluation of the expression.
If a syntax error occurs, the code sets the result to “Syntax Error!” and returns it.
The powerBaseGetter() function extracts the base of each power operation in the expression string.
The factorialNumGetter() function extracts the number being factorialized in each factorial operation in the expression string.

The showPowerOnUi() function takes three arguments: an object data, a string formula, and a number powerNum. The function pushes the string “^(” to the data.operation array, followed by the formula string and the powerNum number. It then pushes the formula string and the powerNum number to the data.formula array.
The trigo() function takes two arguments: a callback function and an angle. If the RADIAN variable is false, the function converts the angle from degrees to radians. The function then calls the callback function with the angle as an argument and returns the result.
The inv_trigo() function takes two arguments: a callback function and a value. If the callback function is not atan and the value is less than -1 or greater than 1, the function displays an alert message and returns NaN. Otherwise, the function calls the callback function with the value as an argument and returns the result. If the RADIAN variable is false, the function converts the result from radians to degrees.

The factorial() function takes a number as an argument. If the number is not an integer, the function calls the gamma() function with the number plus one as an argument and returns the result. If the number is 0 or 1, the function returns 1. Otherwise, the function calculates the factorial of the number using a for loop and returns the result. If the result is Infinity, the function returns Infinity.
The gamma() function takes a number as an argument. If the number is less than 0.5, the function returns the gamma function of 1 minus the number using the formula Math.PI / Math.sin(n * Math.PI) / gamma(1 - n). Otherwise, the function calculates the gamma function of the number using the formula Math.sqrt(2 * Math.PI) * Math.pow(t, n + 0.5) * Math.exp(-t) * x, where t = n + g + 0.5, x = p[0] + sum(p[i] / (n + i)), and g = 7 and p is an array of constants.

