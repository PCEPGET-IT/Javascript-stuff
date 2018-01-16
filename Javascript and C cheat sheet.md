Hi everyone! This is the definitive cheat sheet that will cover everything we did in the last two weeks of coding lessons and hopefully make javascript easier to understand.

## Doing Math in Javascript
* \+ is addition
* \- is subtraction
* / is division
* \* is multiplication
* % gives the remainder when you divide by a number
* \++ increments the integer by 1
* \-- decrements the integer by 1

```javascript
console.log(600 + 700);
// gives 1300

console.log(600 - 700);
// gives -100

console.log(400 / 2);
// gives 200

console.log(2 * 4);
// gives 8

console.log(5 % 2);
// gives 1 because 5 divided by 2 is 2 with a remainder of 1
```

## Variables
Variables store information so that you can use information without typing it over and over. Variables also can change throughout your program.

So there are several different types of variables in C and Javascript
* Integer, which is negative and positive numbers without decimals
* Float, which is a decimal number
* Double, which is a decimal number like a float, but it has more decimal places
* Character(C language specific), is just one letter. To be fair, you don't really need words for Robots
* String(Javascript), is a bunch of words and it's called a string because it's a *string* of characters. (hilarious) 
* Boolean(Javascript) is a true or false value

For Javascript, all you have to do to declare a variable is to type "**var**" and the name of the variable. Note that the variable name can't start with a number, but you can put a number in the name somewhere else.

**Important!** Always end each line of code with a semicolon.

Quick Examples for javascript:
```javascript
// Integer
var distance = 100;

// Decimal
var money = 292.38;

// String
var newstring = "I am a string!";

// Boolean
var lie_detected = true;
```

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

### Why are variables important?
Variables are important because they allow you to store data into a box that makes your programs more useful and easier to adapt. For example, in our earlier variable examples, we had the variable "money". If we were making a money app, we don't want to write out all the numbers because then we limit our program to those specific numbers and we have to type a lot. By putting the amount of money into a variable, we can modify the money data. We can also just type the word "money", and the value that's stored into the variable is used. 

Basically, think of a variable as a box that can hold information. You can carry the box around and use it wherever you go, and you can open the box to change what is inside. Since different boxes are separate from each other, you can have different variables with the same value

Javascript example:
```javascript
var money = 400;
var rent = 400;
```

You can change the variable number later by writing the variable name and writing a new value

```javascript
money = 600;
```

We can also use math operators to change the value of the variables

In this example, we set the variable money to 600 no matter what the original value of the variable was:
```javascript
money = 600;
```

Let's say that we just wanted to decrease the amount of money by $200 because we bought a TV:
```javascript
money = money - 200;
console.log(money);
// gives 400
```

What's going on here?
The equal sign is a way to put a value into the variable. The left side is the variable name, and the right side is the new value that you're changing the variable into. 

By using the variable name in the right side, we are telling the computer to take the value of the variable, change the value, and then assign the new value to the variable again. So instead of just declaring `money = 400`, we can decrease the amount of money by 200 and it doesn't matter what the original value is. 

For math operators you can shorten the syntax.
Instead of
```javascript
money = money - 200;
```
You can just put the math operator before the equal sign and just put the number:
```javascript
money -= 200
// this is the same thing!
```

## Conditionals

What is a condition? A condition tests whether something is true or false. It will seem kind of silly right now, but it is useful later.

So what kind of tests can we do?
Well you can compare two different numbers.
* == tests whether two things are equal
* > tests if one thing is greater than the other
* >= tests if one thing is greater than or equal to the other thing
* < tests if one thing is greater than the other
* <= tests if one thing is greater than or equal to the other thing
* != tests if one thing is not equal to the other thing

If the two numbers make the statement true, then the condition is true. Otherwise, it is false.

In javascript: 
```javascript
    console.log(5 < 4)
    // false
    console.log(4 < 5)
    // true
```

I was really tempted to use the word "return" so I'll define it here. Return means that the program gives that number back to you or another function. 

## and, or logic

## if statements
```javascript 
if(condition is true){
  put code here
} 
```

## while loops

## for loops

## functions

