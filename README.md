# sit323-737-2024-t1-prac4c
W4, credit task

"a. Additional Arithmetic Operations
Expand the capabilities of the calculator microservice by introducing support for advanced arithmetic operations such as exponentiation, square root, and modulo operations. You need to implement corresponding API endpoints to handle these operations, thereby enriching the functionality of the microservice and providing users with more comprehensive calculation capabilities.

OR

b. Error Handling:
Enhance the error handling mechanism of the microservice to deliver more informative error messages to clients. You need to refine error detection and reporting mechanisms, addressing scenarios such as invalid inputs and division by zero. By improving error handling, students will enhance the usability and reliability of the microservice, ensuring a smoother user experience."


Getting started:
- git clone <repository>
- npm install 
- either run node calculatorwithlogger.js OR nodemon from the folder 
- in web browser, go to one of the following locations: 

localhost:3040/{action}?n1={n1}&n2={n2}

Substitutions:

{action} with add, sub, mult, div, exp, mod or sqrt

{n1} and {n2} with numbers. 

Note that decimals are valid numbers for all operations, and negative numbers are valid for most. 

Examples - 

Addition: {n1} + {n2}
1) localhost:3040/add?n1=3&n2=4
Expected result: 7

Subtract: {n1} - {n2}
1) localhost:3040/sub?n1=3&n2=4
Expected result: -1

Multiplication: {n1} * {n2}
1) localhost:3040/mult?n1=3&n2=4
Expected result: 12

Division: {n1} / {n2}
1) localhost:3040/div?n1=3&n2=4
Expected result: 0.75
2) Error handling:
    a) localhost:3040/div?n1=74&n2=0
    Expected result: Error: Cannot divide by zero. 

ADDITIONAL OPERATIONS: 
Exponentiation {n1} ^ {n2} 
1) localhost:3040/exp?n1=2&n2=4
Expected result: 16

Square root: √{n1} 
1) localhost:3040/sqrt?n1=25
Expected result: 5
2) Error handling:
    a) localhost:3040/sqrt?n1=25&n2=44
    Expected result: 5 (as second param set to zero automatically)
    b) localhost:3040/sqrt?n1=-25
    Expected result: Error: Cannot square root a negative number

Modulo {n1} % {n2} 
1) localhost:3040/mod?n1=10&n2=5
Expected result: 0
2) localhost:3040/mod?n1=10&n2=3
Expected result: 1


Notes:

Each API endpoint refers to the same error handling function (specifically errorHandling() here) which validates numbers using validateNumbers(). For this to work, each end point must pass in their operation name.

This set up allows for specific edge cases (such as dividing by zero) to be resolved in the number validation/error handling functions. It also means that further adjustments (such as including additional operations) can be implemented with their specifics quite easily. 