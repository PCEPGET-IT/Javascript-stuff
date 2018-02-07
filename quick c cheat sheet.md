Table of Contents

[General C stuff](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#general-c-stuff)
* [Doing Math in C](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#doing-math-in-c)
* [Variables](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#variables)
* [Conditions](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#conditionals)
* [AND/OR logic](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#and-or-logic)
* [If statements](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#if-statements)
* [Else statements](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#else-statements)
* [Else If statements](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#else-if-statements)
* [While loops](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#while-loops)
* [For loops](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#for-loops)
* [Functions](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#functions)
* [Parameters](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#parameters)
[RobotC stuff](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#robotc-specific-stuff)
* [Motors](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#motorsmoving)
* [Wait](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#waiting)
* [Motor Encoder](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#motor-degrees)
* [Sensor Values](https://github.com/PCEPGET-IT/Javascript-stuff/blob/master/quick%20c%20cheat%20sheet.md#sensor-values)

The quick cheat sheet


# General C stuff

## Doing Math in C
* \+ is addition
* \- is subtraction
* / is division
* \* is multiplication
* % gives the remainder when you divide by a number
* \++ increments the integer by 1
* \-- decrements the integer by 1

## Variables
Variables store information so that you can use information without typing it over and over. Variables also can change throughout your program.

So there are several different types of variables in C and Javascript
* Integer, which is negative and positive numbers without decimals
* Float, which is a decimal number
* Double, which is a decimal number like a float, but it has more decimal places
* Character(C language specific), is just one letter. To be fair, you don't really need words for Robots

**Important!** Always end each line of code with a semicolon.

For C, you have to tell the computer what kind of variable you're declaring. 

* **int** for integer
* **float** for float
* **double** for double
* **char** for character

```c
// Integer
int distance = 100;

// Float
float money = 292.38;

// Double
double pi = 3.1415626535;

// Character
char ch = 'a';
```

Quick math shortcuts for variables:
```c
int number = 10;
number += 10;
// is the same as:
number = number + 10;

number -= 10;
// is the same as:
number = number - 10;

number *= 2;
// is the same as:
number = number * 2;

number /= 2;
// is the same as:
number = number / 2;

number++;
// is the same as:
number = number + 1;

number--; 
// is the same as:
number = number - 1;
```

## Conditionals

Comparing two different numbers.
* == tests whether two things are equal
* \> tests if one thing is greater than the other
* \>= tests if one thing is greater than or equal to the other thing
* < tests if one thing is greater than the other
* <= tests if one thing is greater than or equal to the other thing
* != tests if one thing is not equal to the other thing

If the two numbers make the statement true, then the condition is true. Otherwise, it is false.

## AND OR logic

AND is a type of comparison. It takes two things and sees if both things are true. You write it out like this `&&`

OR is another type of comparison. It takes two things and sees if at least one thing is true. You write it out like this `||` (those are pipes, and you press shift and press the button to the right of the right curly bracket key)

```javascript
console.log(true && true);
// gives true

console.log(true && false);
// gives false

console.log(false && false);
// gives false

console.log(true || true);
// gives true

console.log(true || false);
// gives true

console.log(false || false);
// gives false
```

Another logic boolean thingy is "NOT". It doesn't compare two things, but it flips the true or false value to be the opposite. NOT is used as "**!**"

```javascript
console.log(!true);
// gives false

console.log(!false);
//gives true
```

## if statements

If statements only run a block of code if the condition is true. 
```javascript 
if (condition) {
	// put code here
	// only runs if condition is true
} 
```

If the condition is false, then the program skips the code inside the curly brackets.

## else statements

Else statements run when the condition in the if statement is false.
```javascript 
if (condition) {
	// put code here
	// only runs if condition is true
} 
else {
	// put code here
	// runs if condition is false		
}
```

## else if statements

Else if statements run if the condition in the if statement is false, and the condition in the else if is true

```javascript
if (condition1) {
	// put code here
	// runs if condition1 is true
}
else if (condition2) {
	// put code here
	// runs if condition2 is true (and condition1 is false)
}
else {
	// put code here
	// runs if nothing else runs
}
// rest of code runs
```

## while loops

While loops do something over and over again until the condition is false. 

```javascript
while (condition) {
	// run code until condition is false.
}
```

Try not to make the  while loop go on forever, or you'll get an infinite loop.

## for loops

In C:
```c
for (int i = 0; i < 10; i++){
	// run code ten times
}
```
The for loop can be written as a while loop, but here the variable is local to the for loop which means that other functions can't access the variable. 

This for loop is basically the same thing as this:
```c
int i = 0;
while (i < 10){
	// do something code wise
	i += 1;
	// every time the while loop is run, the variable i increases, so this while loop will only run ten times. 
}
```
This was written using a while loop. 

## functions

In C, you have to tell the computer what value the function will return. These declarations are the same as variables except there's one more:
* void. void means that the function will return nothing

```c
float distance(){
	// this function will measure distance as a decimal number
	return distance;
}
// Don't forget that you can name your code anything you want.
void turnRight(){
	// turn right
	// you don't have to return anything. 
}
```

To use your function, just type it into task main()
```c
turnRight();
```

If you want your program to return something, then type `return` and the information you want to return to the computer. 

You can return a variable that you've made in the function, this variable is local to the function and not accessible by other parts of the function. Previously, we've been defining global variables, which per the name, are accessible anywhere. 

Returning a value allows the function to share its results with other parts of the code, for example, a function to calculate distance and convert distance into number of tire rotations can pass the number of tire rotations to another function that makes the robot move forward for a certain distance. 

**Important: define your functions before task main()!**

## parameters
Functions can also take in inputs. These inputs are called parameters. You just name the parameter and put it into the parantheses of the function. Parameters kind of act like a variable

General form:
```c
int myNewFunction(parameter1){
	// you can use the parameter and modify it. 
	return parameter1;
}
```

Example:
```c
int addTen(number){
	return number + 10;
}
addTen(50);
// gives 60
```

You can have multiple parameters, just type them out and separate them with a comma.

```c
int addTogether(number1, number2){
	return number1 + number2;
}
```

# RobotC specific stuff

## Motors/Moving

```c
motor[motorA] = 25; // setting the power of motor A to 25
motor[motorB] = -30; // sets the power of motor B to go backwards at 30
```

## Waiting

This makes your robot do what it's currently doing for a certain amount of time
```c
wait1Msec(milliseconds)
// put the time you want in milliseconds between the parantheses. 1000 milliseconds = 1 second
```

## Motor Degrees

This helps measure the amount of degrees a motor has traveled, and it can also reset the encoder when you need a fresh reading. 

Resetting the encoder:
```c
nMotorEncoder[motorA] = 0;
```

Grabbing the value from the encoder:
```c
while(nMotorEncoder[motorA] < 180){
	motor[motorA] = 30;
}
```
This means that "while" the amount of degrees that motor A has traveled is less than 180 degrees, move motor A forward at a power of 30. 

## Sensor Values

Go into the menu of Robot > Motors and Sensor Setup
Go to Sensors
Choose your sensor and name the sensor. This is the name you will be using in your program. 

This will access the value of the sensor:
```c
SensorValue(sensor_name_here)
```

Light sensors return a number from 0-100, 0 means no light reflected (black), and 100 means all the light is reflected (aluminum foil).

Touch sensors return 0 or 1, 0 is not pressed, 1 is pressed.

Ultrasonic sensors return a distance, the units are chosen in the Motors and Sensor Setup. 

Example of using SensorValue:
```c
// light sensor is named leftLight
int lightThresh = 35;
while(SensorValue(leftLight)>lightThresh){
	motor[motorB] = 25;
	motor[motorC] = 0;
}
```
