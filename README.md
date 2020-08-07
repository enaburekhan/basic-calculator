# basic-calculator
# Designed by Eric Enanurekhan

The layout of the Basic calculator app was crafted using CSS grid and flex-box.
It consist of five different sets of key buttons that are all children of the calculator-keys class.
They include: the digits(0 = 9), operator(+,-,*,/ and =), a reset(AC), delete and decimal keys. All these keys are been listened to by the calculator to return their type by adding the keys.addEventListener('click', (event) => ...) function using event delegation.
seven functions were created to achieve the functionality of the APP.
1. function updateDisplay():
    This function is invoked anytime an operation is performed in the app to update the screen with the contents of the displayValue.
2. function inputDigit(digit):
    This function uses a ternary operator(?) to check if the current value displayed on the calculator is zero. If so, it overrides it with new input value. Otherwise, it appends to it.
3. function inputDecimal(dot):
    It uses the includes() method to check if the displayValue does not already contain a decimal point. If so, a dot is appended to the number. Otherwise, the function exits.
4. function handleOperator(nextOperator):
    This function enables the contents of displayValue to be converted to floating-point number and the result stored in the firstOperand property. The operator property is also set to whatever operator key was clicked while waitingForSecondOperand is set to true which indicates that the first operand has been entered and whatever digits the user enters next will constitute the second operand.
5.  function calculate(firstoperand, secondOperand, operator):
     This function takes the first operand, second operand and operator as arguments and checks the value of the operator to determine to determine how the expression should be evaluated. If the operator is =, the second operand will be returned.
6.  function deleteText():
     This function uses the .pop() method to remove each displayValue on each click after being split.
7.  function resetcalculator():
     This function sets all the properties of the calculator object to their original values.          
       
       
       