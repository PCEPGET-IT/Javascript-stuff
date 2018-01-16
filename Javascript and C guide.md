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

Basically, think of a variable as a box that can hold information. You can carry the box around and use it wherever you go, and you can open the box to change what is inside. Since different boxes are separate from each other, you can have different variables with the same value.

Another analogy is that variables are just like labels, and they point to data. By using a variable you're telling the computer to use the data that is labelled by the variable. Changing data is just like taking the label off and putting it on something else.

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
* \> tests if one thing is greater than the other
* \>= tests if one thing is greater than or equal to the other thing
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

I was really tempted to use the word "return" so I'll define it here. Return means that the line of code gives that value back. It's kind of like console.log, but for computers. console.log prints out a value for you to see, while return gives the value to the program to use. 

So when you evaluate (or test) a conditional, that code line will return `true` or `false`. 

Similarly, doing math returns a number. That number is quickly lost unless you assign it to a variable, then the number stays around and you can use it. 

This could be useful if you're testing variable values to make sure that they meet certain criteria. Much like how if you're hiring someone, you want them to be nice and competent.

Back to our money example. Let's declare two variables, one for our money, and one for the cost of the TV.

```javascript
var money = 400;
var TVcost = 200;
```

Now we want to make sure that we have enough money to buy a TV. What do we do?

We can use a greater than or equal comparison!
```javascript
console.log(money >= TVcost);
//gives true
```

This means that we can buy that TV!

If we changed our `money` variable to 100, then the console.log will give us false, which means that we don't have enough money to buy it. 

## and, or logic

And or logic also helps return true or false values. They are part of what is known is boolean logic. Booleans only have the values true and false. (What was discussed in the conditional section is part of booleans).

And is a type of comparison. It takes two things and sees if both things are true. You write it out like this `&&`

Or is another type of comparison. It takes two things and sees if at least one thing is true. You write it out like this `||` (those are pipes, and you press shift and press the button to the right of the right curly bracket key)

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

Alright, that is helpful. But that doesn't look useful in a program.

Well you can join comparisons and and/or logic things together!

```javascript
console.log(5 > 4 || -100 > 4);
// gives true
```
Let's break this down. So computers first evaluate the number comparisons and then do the `&&, ||, !` thing.

Is 5 greater than 4? Yes, or in computerland, true!
Is -100 greater than 4? No, or in computerland, false.

Now we can substitute true and false into the expression to make it...
```javascript
console.log(true || false);
```

Hmmm. So Or means that at least one thing is true, so true or false means that it is true. 

Alright that's marginally more useful you think. Imagine if we put a variable into the statement. Now that has a lot of potential. 

So let's say that you're buying a TV. According to our earlier example, as long as you have more money than the TV cost, then you can buy it. What if you wanted to have a certain amount of money left over for paying rent? You can't buy a TV with only $1 left over, that's silly.

Let's define three variables, money, rent, and the cost of the TV:
```javascript
var money = 600;
var rent = 500;
var TVcost = 200;
```

Alright, so we want to make sure that we have enough money to buy the TV, so let's get that set up:
```javascript
console.log(money >= TVcost);
// gives true
```

Now we can add our second condition to the first condition. Our second condition is that we have to have money left over to pay the rent. So the money left over after paying the TV is `money - TVcost` and we want that to be greater than or equal to the rent. So our final condition statement is `money - TVcost >= rent`. 

Now we have both of our conditions, now we need to combine the two statements. We should use the AND operator because we only want both things to be true. 

```javascript
console.log(money >= TVcost && money - TVcost >= rent);
// gives true
```

To be honest, you could simplify this expression into something like this:
```javascript
console.log(money - TVcost - rent >= 0);
//gives true
```

I just wanted to show an example of where you could use the boolean operators. With robotic sensors, these boolean operators will be very useful.

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

In javascript:
```javascript
for (var i = 0; i < 10; i++){
	// run code for a certain number of times
	// in this example, this code will run 10 times.
}
```
In C:
```c
for (int i = 0; i < 10; i++){
	// run code ten times
}
```
The for loop can be written as a while loop, but here the variable is local to the for loop which means that other functions can't access the variable. 

This for loop is basically the same thing as this:
```javascript
var i = 0;
while (i < 10){
	// do something code wise
	i += 1;
	// every time the while loop is run, the variable i increases, so this while loop will only run ten times. 
}
```
This was written using a while loop. 

## functions
Functions are just an easy way to name a set of instructions so that you don't have to write out the same instructions over and over. For example if you a lot of tipping and tax instructions in your program, then you should put these instructions into a function. 

It's kind of like how we use a variable to represent data that we don't want to type over and over and be flexible. We use a function to represent instructions that we don't want to type over and over. And if we realize that we typed the function wrong, we can fix it once and the program can run correctly. 

In javascript, you just type:
```javascript
function yourFunctionName(){
	// insert code here
	// OPTIONAL:
	return value;
}
```

You can name your function whatever you want, just remember to put () after the function name. 

If you want your program to return something, then type `return` and the information you want to return to the computer. 

You can return a variable that you've made in the function, this variable is local to the function and not accessible by other parts of the function. Previously, we've been defining global variables, which per the name, are accessible anywhere. 

```javascript
function myNewFunction(){
	var testvar = 40;
	testvar += 40
	return testvar;
}
console.log(testvar);
// gives error because testvar is not defined globally. 
console.log(myNewFunction());
// returns 80
```

In C, you have to tell the computer what value the function will return. These declarations are the same as variables except there's one more:
* void. void means that the function will return nothing

```c
float distance(){
	// this function will measure distance as a decimal number
	return distance;
}
void turnRight(){
	// turn right
	// you don't have to return anything. 
}
```

Returning a value allows the function to share its results with other parts of the code, for example, a function to calculate distance and convert distance into number of tire rotations can pass the number of tire rotations to another function that makes the robot move forward for a certain distance. 

Of course you can just combine two functions into one function by itself, but you need to think about whether it is useful to have two separate functions or to have one function. In this case, I think that combining the two functions would be more concise as each function separately doesn't seem that helpful. Judging code decisions gets easier with practice, so don't be scared of making mistakes.

Functions can also take in inputs. These inputs are called parameters. You just name the parameter and put it into the parantheses of the function. Parameters kind of act like a variable

General form:
```javascript
function myNewFunction(parameter1){
	// you can use the parameter and modify it. 
}
```

Example:
```javascript
function addTen(number){
	return number + 10;
}
console.log(addTen(50));
// gives 60
```
In this function, we tell the computer "I want to make a function named addTen. I also want this function to take one input named number". Then we tell the computer that when we call this function (calling a function means typing out the function to use it) we take the parameter named number, and we add ten and return that number. 

So when we call that function with the input 50, the function takes 50 and adds ten, which gives us 60. 

You can have multiple parameters, just type them out and separate them with a comma.

```javascript
function addTogether(number1, number2){
	return number1 + number2;
}
```

## Organizing your code

Try to space everything out so it looks nice. Sometimes you get a flash of inspiration, and you just want to code everything. Please still try to indent each new instruction, and you can space out everything nicely later. Although indenting automatically is encouraged.

When should you indent?
Indent the stuff that is inside {}. So like while loops, if, else, else ifs, functions, etc. 

Also, try to plan your code out before you actually start programming. A good way to do this is through a flow chart, and write instructions in plain English. This is called "Pseudocode".

A really good thing to do is to add comments.

In C, you type `//` for a single line comment.
You type `/*` and `*/` for a multiline comment.

```c
// I am a single line comment!
/* I am a multiline comment
look at my multi-ness */
```

Okay, I think that's it, this is the really huge guide, and then the cheatsheet will be posted later. 