Hi everyone! This is the definitive cheat sheet that will cover everything we did in the last two weeks of coding lessons and hopefully make javascript easier to understand.

## Doing Math in Javascript
* \+ is addition
* \- is subtraction
* / is division
* \* is multiplication

## Variables
Variables store information so that you can use information without typing it over and over. Variables also can change throughout your program.

So there are several different types of variables in C and Javascript
* Integer, which is negative and positive numbers without decimals
* Float, which is a decimal number
* Double, which is a decimal number like a float, but it has more decimal places
* Character(C language specific), is just one letter. To be fair, you don't really need words for Robots
* String(Most other languages have this), is a bunch of words and it's called a string because it's a *string* of characters. (hilarious) 

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

## if statements
```javascript 
if(condition is true){
  put code here
} 
```
