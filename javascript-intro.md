## What is Computer Programming

**Computer programming** is the process of designing and building an [executable](https://en.wikipedia.org/wiki/Executable) [computer program](https://en.wikipedia.org/wiki/Computer_program) to accomplish a specific [computing](https://en.wikipedia.org/wiki/Computing) result or to perform a specific task. [[1](https://en.wikipedia.org/wiki/Computer_programming)]

Computer’s however don’t understand English, in order to tell a computer what to do, we need a programming language. 

**Programming Language**

A programming language is a series of symbols and numbers that allow humans to speak in a language the computer will understand, 0’s and 1’s. (Binary) [[2](https://www.codecademy.com/resources/blog/programming-languages/)]

**JavaScript** 

JavaScript is a programming language that can be used to create all sorts of computer programs. Mobile applications, web applications, even desktop applications can be created using JavaScript. It’s awesome!  

**Why JavaScript for this course?**

1. Relatively straightforward syntax. 
2. Easy to get started with little extra setup. 
3. Most entry level programming jobs are in the field of web development, where JavaScript is essential. 

## Variables

A variable is a container that stores a value. [[3](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)] When **declaring** a variable you use the **let** keyword followed by the name of the variable.

Ex: <code>let hello;</code></strong>

Note the semicolon at the end, this indicates the end of the statement, however, strictly speaking it is generally not needed.

In order to **assign **a value to the variable you use an equals sign.

Ex: `hello = 'hello'`

This can also be done on one line. 

Ex: <code>let hello = 'hello'</code></strong>

A variable's value can be reassigned to a new value. 

```
hello = 'not hello'
```

A variable’s value can is not limited to a string, (text), it can be all sorts of different **data types**. 

Variable names are case sensitive, hello is not the same as Hello. Variable names can not start with a number and can not include a space between them. 

JavaScript convention dictates that variable names use the camelCase convention. The first word starts lower case, with each subsequent word capitalized. 

Note: For variables where we don’t want to change the value, we can use the keyword **const**

## Booleans

A boolean data type refers to true and false. We will often want to check if a value is **true** or **false**, and based on that information either perform, or not perform a certain set of instructions.

Ex: <code>let bool = false; </code></strong>

Ex: <code>bool = <strong>true</strong>;</code>

Basic Data Types

Javascript has nine types, we won’t cover or use all of them, so far we have seen a **string** which holds a text value in either single or double quotes. We have also seen a **boolean**, which is a value holding true or false. We will also explore other types, like **number**, **object** , and **function**. 

## Operators

An operator represents an action. We have mathematical operators (+, -, *, /). We already covered another important operator (=, assignment). 

Some other important operators are **===** for checking if two values are equal, **!==**, check if two values are not equal. Placing an (!) in front of a value turns the value from true - false, and false to true. 

## Conditionals


```
let favorite = 'hamburger'
 
let result;
 
if(favorite === 'pizza'){
    result = "That's my favorite"
}else {
    result = "That's not my favorite."
}
```


The **if **evaluates what’s inside the parentheses as a boolean. If the boolean is true, the code in the blocks runs, otherwise whatever is in the else block will run. 

The code above is referred to as an if/else statement. An if statement, does not NEED to be paired with an else, but often is.

Similar to the if, is the **else if, **an else if, follows a proceeding if (or else if), and performs the same as an if statement. 

    let favorite = 'hamburger'  
      
    let result;  
      
    if(favorite === 'pizza'){  
    	result = "That's my favorite"  
    }else {  
    	result = "That's not my favorite."  
    }

If/else statements allow us to control the **flow** of the program. 

Our program above, stores a value in result, however, nothing is really done with this value. Let’s change that by printing out the value of the result. 

    let favorite = 'hamburger'  
      
    let result;  
      
    if(favorite === 'pizza'){  
	    result = "That's my favorite"  
    }else  if(favorite === 'hamburger'){
    	result = "That's my second favorite"
    }else {  
    	result = "That's not my favorite."  
    }

The console.log() is a very powerful tool which we will use a lot in order to see values. In order to understand how it works, we will need a lot more background, so for now, just think of it as a command to print something to the screen.

Where can we run this code?

For now we will run our code using this [website](https://replit.com/languages/nodejs/), but will later explore other methods. 

## Logical Operators

We can do more interesting checks in the code flow using logical operators, **||** (or), **&& **(and)

Using logical operators we can evaluate statements to be true or false. 

![Truth Table](https://i.stack.imgur.com/nl0W8.jpg)

```
const a = false;
const b = true; 

console.log(a && b)
console.log(a || b)
```


## Looping Code

If you want to perform some piece of code multiple times, instead of writing the code line by line you can use a loop to execute a certain piece of code throughout a number of iterations. 

Suppose we wanted to log out to the user the numbers 1 -10. We could write out 10 lines of code, and log each number 1 - 10. That’s doable, although certainly annoying. This becomes less feasible if you want to go up to 100 (or higher)


```
for (let i=1; i < 11; i++){
    console.log(i)
}
```


The** for loop** is used when you want to loop over a certain **code block **(code in between curly braces) a known amount of iterations. There are a few basic components of the for loop. [[4](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)]



1. The keyword **for** followed by parentheses
2. An **initializer** → In this case i = 1. This is used to keep track of how many iterations are left in the loop. 
3. A **condition** → As long as this condition evaluates to true, the loop will continue to execute code. 
4. **Final-expression** → A piece of code executed at the end of the loop. Generally used to increment the initializer. (Note: the ++ operand, is shorthand for incrementing a number by 1)
5. The **code block** → The code in curly braces that gets executed each iteration of the loop. 

For loops become even more powerful when using conditional logic inside of them.


```
for (let i=1; i < 11; i++){
    if(i === 2){
        console.log('2 is my favorite number')
    }else{
        console.log(i)
    }
    
}
```


## Comments

Comments are used to explain to a programmer certain pieces of the code to refer to later. A comment can either be written using two forward slashes. Everything following the two forward slashes will not be read/interpreted by the computer. 

For multi-line comments: A forward slash, followed by an asterisk, closed out by an asterisk and a forward slash.


```
/* comment line 1
Comment line 2 */
```


## Functions

A function is used when you have repeated logic inside of your code. Instead of repeating the same code wherever we need, we can use a function to encapsulate the shared logic. 

Functions start with the keyword **function **followed by the function’s name, then parentheses , inside of which can optionally hold **parameters**, finally a code block to be executed when the function is **invoked. **


```
function multiplyByTwo(num){
    return num * 2;
}

const multiplied = multiplyByTwo(4)

console.log(multiplied)
```


Notice the variable num, this is the parameter. This variable could be given any name, however it’s best to pick a name that makes sense in context of the function. Inside of the function we multiply “num” by 2. We also have a **return** statement, which tells the function what value the function should return. 

A function does not **need** to have a return value, for example instead of returning the value, it could have been logged out to the console. 

A function lays dormant until it is called or **invoked**. When you invoke a function you pass it any **arguments** that the function is expecting to receive. In the above example, the number 4 is the only argument, and it’s invoked inside of parentheses. 

Note: A function has its own **scope**, which means you can’t access any values inside of the function, outside of the function. Meaning the variable num only exists while inside of the function. You would not be able to log out num to the console.

## Objects

An object is a collection of properties. A property consists of a key/value pair. [[5](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)] An object is initialized and inside the curly braces contains the object's properties. An object can often mimic real life objects, hence the name.


```
const person = {
    name: 'John Doe',
    age: 32,
    eyeColor: 'blue',
    allergies: false,
    greeting: function(){
        return 'Hello my name is ' + this.name + ' i am ' + this.age + ' years old.'
    }
}
```


We initialized our object with assorted key/value pairs, which we can then access in one of two ways.



1. Dot notation. Ex: `console.log(person.age) ` The name of the object followed by a dot and the property name returns the value stored.
2. Bracket notation. Ex: `console.log(person['age']) ` Bracket notation works almost exactly the same, it’s important to note the property is accessed using a string inside of the square brackets. If you don’t use a string “age” will be read as a variable instead. 

You want to use bracket notation if your object’s property has more than one word, or if you are using a variable. Otherwise use dot notation. 

Notice the property greeting contains a function as value. When a function is used as a value, this is referred to as a **method**.

When invoking a method the **this** keyword refers to the object on which the method is being called. For example, in this case this.name would be “John Doe”. 

We can also add, remove, or change property values. 



1. Adding: `person.weight = 150 `We add values the same way we assign variable values.
2. Removing: <code>delete person.allergies </code></strong>We use the <strong>delete</strong> operand in order to remove a property from an object.
3. Changing: <code>person.allergies = <strong>true </strong></code>We change values the same we assign them.

If we go back to console.log(), we now have all the tools to understand what’s happening. Console is an object, and log is a method. 

## Arrays

Arrays are used to store a collection of elements which can be iterated over. Arrays are full of built in methods that can be used for iterating over them, manipulating them, and getting more data from them. 

**Creating an array**: <code>const colors = ['red', 'blue']</code></strong>

We use the square brackets on either end when initializing an array. Arrays are composed of comma separated values (or elements). 

**Getting** the value of an element: Unlike objects that have a key, array’s do not have a key. You need to use an **index** to access a specific element. 

Arrays are indexed from 0. So the first element of the array can be accessed using the array name, followed by square brackets, and the number 0 is inside. console.log(colors[0])

We can **change** the value of an array in a given index as follows: `colors[1] = 'green'`

**Adding** an item at the end of the array you can use the built in .push() method. 

**Removing** an item from the end of the array .pop()

Often we will want to know the length of the array, the built it .length property returns the number of elements in the array. 

Arrays are great for iterating over. The most basic method for iterating over an array: 


```
const colors = ['red', 'orange', 'yellow', 'green', 'blue']

for (let i=0; i < colors.length; i++){
    console.log('The color at index ' + i + ' is ' + colors[i])
}
```


Combining loops and arrays is a very powerful combination that allows us to make very interesting and powerful applications. 
