# JavaScript

## What is JavaScript?

**A high-level definition**
JavaScript is a scripting or programming language that allows you to implement complex features on web pages — every time a web page does more than just sit there and display static information for you to look at — displaying timely content updates, interactive maps, animated 2D/3D graphics, scrolling video jukeboxes, etc. — you can bet that JavaScript is probably involved. It is the third layer of the layer cake of standard web technologies, two of which (HTML and CSS) we have covered in much more detail in other parts of the Learning Area.

- HTML 
 is the markup language that we use to structure and give meaning to our web content, for example defining paragraphs, headings, and data tables, or embedding images and videos in the page.

- CSS 
  is a language of style rules that we use to apply styling to our HTML content, for example setting background colors and fonts, and laying out our content in multiple columns.

- JavaScript
   is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else. (Okay, not everything, but it is amazing what you can achieve with a few lines of JavaScript code.)

The three layers build on top of one another nicely. Let's take a simple text label as an example. We can mark it up using HTML to give it structure and purpose:

<p>Player 1: Chris</p>



Then we can add some CSS into the mix to get it looking nice:

p {
  font-family: "helvetica neue", helvetica, sans-serif;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-align: center;
  border: 2px solid rgba(0, 0, 200, 0.6);
  background: rgba(0, 0, 200, 0.3);
  color: rgba(0, 0, 200, 0.6);
  box-shadow: 1px 1px 2px rgba(0, 0, 200, 0.4);
  border-radius: 10px;
  padding: 3px 10px;
  display: inline-block;
  cursor: pointer;
}

And finally, we can add some JavaScript to implement dynamic behavior:


const para = document.querySelector('p');

para.addEventListener('click', updateName);

function updateName() {
  const name = prompt('Enter a new name');
  para.textContent = `Player 1: ${name}`;
}


## So what can it really do?

The core-client-side JavaScript language consists of some common programming features that allow you to do things like:

- Store useful values inside variables. In the above      example  for instance, we ask for a new name to be entered then store that name in a variable called name.

- Operations on pieces of text (known as "strings" in programming). In the above example we take the string "Player 1: " and join it to the name variable to create the complete text label, e.g. "Player 1: Chris".

- Running code in response to certain events occurring on a web page. We used a click event in our example above to detect when the label is clicked and then run the code that updates the text label.

- And much more!


## Storing the information you need Variables

### What is a variable?

A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.

Variable example
Let's look at a simple example:

<button id="button_A">Press me</button>
<h3 id="heading_A"></h3>


const buttonA = document.querySelector('#button_A');
const headingA = document.querySelector('#heading_A');

buttonA.onclick = () => {
  const name = prompt('What is your name?');
  alert(`Hello ${name}, nice to see you!`);
  headingA.textContent = `Welcome ${name}`;
}


In this example pressing the button runs some code. The first line pops a box up on the screen that asks the reader to enter their name, and then stores the value in a variable. The second line displays a welcome message that includes their name, taken from the variable value and the third line displays that name on the page.



An aside on variable naming rules
You can call a variable pretty much anything you like, but there are limitations. Generally, you should stick to just using Latin characters (0-9, a-z, A-Z) and the underscore character.

You shouldn't use other characters because they may cause errors or be hard to understand for an international audience.
Don't use underscores at the start of variable names — this is used in certain JavaScript constructs to mean specific things, so may get confusing.
Don't use numbers at the start of variables. This isn't allowed and causes an error.
A safe convention to stick to is so-called "lower camel case", where you stick together multiple words, using lower case for the whole first word and then capitalize subsequent words. We've been using this for our variable names in the article so far.
Make variable names intuitive, so they describe the data they contain. Don't just use single letters/numbers, or big long phrases.
Variables are case sensitive — so myage is a different variable from myAge.
One last point: you also need to avoid using JavaScript reserved words as your variable names — by this, we mean the words that make up the actual syntax of JavaScript! So, you can't use words like var, function, let, and for as variable names. Browsers recognize them as different code items, and so you'll get errors.



Good name examples:

age
myAge
init
initialColor
finalOutputValue
audio1
audio2


## Variable types


There are a few different types of data we can store in variables. In this section we'll describe these in brief, then in future articles, you'll learn about them in more detail.

So far we've looked at the first two, but there are others.

## Numbers
You can store numbers in variables, either whole numbers like 30 (also called integers) or decimal numbers like 2.456 (also called floats or floating point numbers). You don't need to declare variable types in JavaScript, unlike some other programming languages. When you give a variable a number value, you don't include quotes:

let myAge = 17;

## Strings


Strings are pieces of text. When you give a variable a string value, you need to wrap it in single or double quote marks; otherwise, JavaScript tries to interpret it as another variable name.

let dolphinGoodbye = 'So long and thanks for all the fish';


## Boonleans

Booleans are true/false values — they can have two values, true or false. These are generally used to test a condition, after which code is run as appropriate. So for example, a simple case would be:

let iAmAlive = true;

Whereas in reality it would be used more like this:

let test = 6 < 3;

This is using the "less than" operator (<) to test whether 6 is less than 3. As you might expect, it returns false, because 6 is not less than 3! You will learn a lot more about such operators later on in the course.



## Arrays


An array is a single object that contains multiple values enclosed in square brackets and separated by commas. Try entering the following lines into your console:

let myNameArray = ['Chris', 'Bob', 'Jim'];
let myNumberArray = [10, 15, 40];
Copy to Clipboard
Once these arrays are defined, you can access each value by their location within the array. Try these lines:

myNameArray[0]; // should return 'Chris'
myNumberArray[2]; // should return 40


## Objects

In programming, an object is a structure of code that models a real-life object. You can have a simple object that represents a box and contains information about its width, length, and height, or you could have an object that represents a person, and contains data about their name, height, weight, what language they speak, how to say hello to them, and more.

Try entering the following line into your console:

let dog = { name : 'Spot', breed : 'Dalmatian' };


To retrieve the information stored in the object, you can use the following syntax:

dog.name


## Dynamic typing

JavaScript is a "dynamically typed language", which means that, unlike some other languages, you don't need to specify what data type a variable will contain (numbers, strings, arrays, etc.).

For example, if you declare a variable and give it a value enclosed in quotes, the browser treats the variable as a string:

let myString = 'Hello';

Even if the value enclosed in quotes is just digits, it is still a string — not a number — so be careful:

let myNumber = '500'; // oops, this is still a string
typeof myNumber;
myNumber = 500; // much better — now this is a number
typeof myNumber;

## Constants in JavaScript

As well as variables, you can declare constants. These are like variables, except that:

you must initialize them when you declare them
you can't assign them a new value after you've initialized them.
For example, using let you can declare a variable without initializing it:

let count;

Similarly, with let you can initialize a variable, and then assign it a new value (this is also called reassigning the variable):

let count = 1;
count = 2;


## Basic math in JavaScript - numbers and operators

We use different terms to describe different types of decimal numbers, for example:

- Integers are floating-point numbers without a fraction. They can either be positive or negative, e.g. 10, 400, or -5.
- Floating point numbers (floats) have decimal points and decimal places, for example 12.5, and 56.7786543.
- Doubles are a specific type of floating point number that have greater precision than standard floating point numbers (meaning that they are accurate to a greater number of decimal places).

We even have different types of number systems! Decimal is base 10 (meaning it uses 0–9 in each column), but we also have things like:

Binary — The lowest level language of computers; 0s and 1s.
Octal — Base 8, uses 0–7 in each column.
Hexadecimal — Base 16, uses 0–9 and then a–f in each column. You may have encountered these numbers before when setting colors in CSS.
Before you start to get worried about your brain melting, stop right there! For a start, we are just going to stick to decimal numbers throughout this course; you'll rarely come across a need to start thinking about other types, if ever.

The second bit of good news is that unlike some other programming languages, JavaScript only has one data type for numbers, both integers and decimals — you guessed it, Number. This means that whatever type of numbers you are dealing with in JavaScript, you handle them in exactly the same way.

Note: Actually, JavaScript has a second number type, BigInt, used for very, very large integers. But for the purposes of this course, we'll just worry about Number values.

It's all numbers to me
Let's quickly play with some numbers to reacquaint ourselves with the basic syntax we need. Enter the commands listed below into your developer tools JavaScript console.

First of all, let's declare a couple of variables and initialize them with an integer and a float, respectively, then type the variable names back in to check that everything is in order:
const myInt = 5;
const myFloat = 6.667;
myInt;
myFloat;
Copy to Clipboard
Number values are typed in without quote marks — try declaring and initializing a couple more variables containing numbers before you move on.
Now let's check that both our original variables are of the same datatype. There is an operator called typeof in JavaScript that does this. Enter the below two lines as shown:
typeof myInt;
typeof myFloat;
Copy to Clipboard
You should get "number" returned in both cases — this makes things a lot easier for us than if different numbers had different data types, and we had to deal with them in different ways. Phew!


## Useful Number methods

The Number object, an instance of which represents all standard numbers you'll use in your JavaScript, has a number of useful methods available on it for you to manipulate numbers. We don't cover these in detail in this article because we wanted to keep it as a simple introduction and only cover the real basic essentials for now; however, once you've read through this module a couple of times it is worth going to the object reference pages and learning more about what's available.

For example, to round your number to a fixed number of decimal places, use the toFixed() method. Type the following lines into your browser's console:

const lotsOfDecimal = 1.766584958675746364;
lotsOfDecimal;
const twoDecimalPlaces = lotsOfDecimal.toFixed(2);
twoDecimalPlaces;
Copy to Clipboard
Converting to number data types
Sometimes you might end up with a number that is stored as a string type, which makes it difficult to perform calculations with it. This most commonly happens when data is entered into a form input, and the input type is text. There is a way to solve this problem — passing the string value into the Number() constructor to return a number version of the same value.

For example, try typing these lines into your console:

let myNumber = "74";
myNumber += 3;
Copy to Clipboard
You end up with the result 743, not 77, because myNumber is actually defined as a string. You can test this by typing in the following:

typeof myNumber;
Copy to Clipboard
To fix the calculation, you can do this:

let myNumber = "74";
myNumber = Number(myNumber) + 3;
Copy to Clipboard
The result is then 77, as initially expected.


## Arithmetic operators

Operator	Name	Purpose	Example
+	Addition	Adds two numbers together.	6 + 9
-	Subtraction	Subtracts the right number from the left.	20 - 15
*	Multiplication	Multiplies two numbers together.	3 * 7
/	Division	Divides the left number by the right.	10 / 5
%	Remainder (sometimes called modulo)	
Returns the remainder left over after you've divided the left number into a number of integer portions equal to the right number.

8 % 3 (returns 2, as three goes into 8 twice, leaving 2 left over).

**	Exponent	Raises a base number to the exponent power, that is, the base number multiplied by itself, exponent times.	5 ** 2 (returns 25, which is the same as 5 * 5).
Note: You'll sometimes see numbers involved in arithmetic referred to as operands.

Note: You may sometimes see exponents expressed using the older Math.pow() method, which works in a very similar way. For example, in Math.pow(7, 3), 7 is the base and 3 is the exponent, so the result of the expression is 343. Math.pow(7, 3) is equivalent to 7**3.





## Control flow:
The control flow is the order in which the computer executes statements in a script.

COde is run in order from the first line in the file to last line, unless the comuer runs across the structures that change the control flow, such as conditionals and loops.

For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:


if (isEmpty(field)) {
  promptUser();
} else {
  submitForm();
}

A typical script in JavaScript or PHP (and the like) includes many control structures, including conditionals, loops and functions. Parts of a script may also be set to execute when events occur.
For example, the above excerpt might be inside a function that runs when the user clicks the Submit button for the form. The function could also include a loop, which iterates through all of the fields in the form, checking each one in turn. Looking back at the code in the if and else sections, the lines promptUser and submitForm could also be calls to other functions in the script. As you can see, control structures can dictate complex flows of processing even with only a few lines of code.

Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution.


## JavaScript Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

Example
// Function to compute the product of p1 and p2
function myFunction(p1, p2) {
  return p1 * p2;
}

## Coding


<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Functions</h2>

<p>This example calls a function which performs a calculation, and returns the result:</p>

<p id="demo"></p>

<script>
function myFunction(p1, p2) {
  return p1 * p2;
}
document.getElementById("demo").innerHTML = myFunction(4, 3);
</script>

</body>
</html>

Result


JavaScript Functions
This example calls a function which performs a calculation, and returns the result:

12

Why Functions????

You can reuse code: Define the code once, and use it many times.

You can use the same code many times with different arguments, to produce different results.

Example
Convert Fahrenheit to Celsius:

function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);

Coding 
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Functions</h2>

<p>This example calls a function to convert from Fahrenheit to Celsius:</p>
<p id="demo"></p>

<script>
function toCelsius(f) {
  return (5/9) * (f-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
</script>

</body>
</html>


Result

JavaScript Functions
This example calls a function to convert from Fahrenheit to Celsius:

25



The () Operator Invokes the Function
Using the example above, toCelsius refers to the function object, and toCelsius() refers to the function result.

Accessing a function without () will return the function object instead of the function result.

Example
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;













JavaScript Function Syntax
A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

function name(parameter1, parameter2, parameter3) {
  // code to be executed
}










JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB and Adobe Acrobat. JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.
JavaScript's dynamic capabilities include runtime object construction, variable parameter lists, function variables, dynamic script creation (via eval), object introspection (via for...in and Object utilities), and source-code recovery (JavaScript functions store their source text and can be retrieved through toString()).

This section is dedicated to the JavaScript language itself, and not the parts that are specific to Web pages or other host environments. For information about APIs that are specific to Web pages, please see Web APIs and DOM.

The standards for JavaScript are the ECMAScript Language Specification (ECMA-262) and the ECMAScript Internationalization API specification (ECMA-402). As soon as one browser implements a feature, we try to document it. This means that cases where some proposals for new ECMAScript features have already been implemented in browsers, documentation and examples in MDN articles may use some of those new features. Most of the time, this happens between the stages 3 and 4, and is usually before the spec is officially published.

Do not confuse JavaScript with the Java programming language — JavaScript is not "Interpreted Java". Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantics, and use.

What is JavaScript?
Welcome to the MDN beginner's JavaScript course! In this first article we will look at JavaScript from a high level, answering questions such as "what is it?", and "what is it doing?", and making sure you are comfortable with JavaScript's purpose.

A first splash into JavaScript
Now you've learned something about the theory of JavaScript, and what you can do with it, we are going to give you a crash course on the basic features of JavaScript via a completely practical tutorial. Here you'll build up a simple "Guess the number" game, step by step.

What went wrong? Troubleshooting JavaScript
When you built up the "Guess the number" game in the previous article, you may have found that it didn't work. Never fear — this article aims to save you from tearing your hair out over such problems by providing you with some simple tips on how to find and fix errors in JavaScript programs.

Storing the information you need — Variables
After reading the last couple of articles you should now know what JavaScript is, what it can do for you, how you use it alongside other web technologies, and what its main features look like from a high level. In this article, we will get down to the real basics, looking at how to work with the most basic building blocks of JavaScript — Variables.

Basic math in JavaScript — numbers and operators
At this point in the course, we discuss maths in JavaScript — how we can combine operators and other features to successfully manipulate numbers to do our bidding.

Handling text — strings in JavaScript
Next, we'll turn our attention to strings — this is what pieces of text are called in programming. In this article, we'll look at all the common things that you really ought to know about strings when learning JavaScript, such as creating strings, escaping quotes in strings, and joining them together.

Useful string methods
Now we've looked at the very basics of strings, let's move up a gear and start thinking about what useful operations we can do on strings with built-in methods, such as finding the length of a text string, joining and splitting strings, substituting one character in a string for another, and more.

Arrays
In the final article of this module, we'll look at arrays — a neat way of storing a list of data items under a single variable name. Here we look at why this is useful, then explore how to create an array, retrieve, add, and remove items stored in an array, and more besides.