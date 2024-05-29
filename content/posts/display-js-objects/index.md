---
title: "How To Display JavaScript Objects"
date: 2024-05-29T15:10:04+05:30
draft: false
tags: ["JavaScript", "objects", "DOM", webdev]
---


While primitives in JavaScript are values themselves, everything else, including arrays and functions, **are objects**. Understanding how to leverage objects in the Document Object Model *(DOM)* is vital for effective web development.  

This is a guide on different methods of displaying Objects when working with the DOM.

____

Displaying a JavaScript Object will output `[object Object]` by default:

```js
const mySelf = {  
    name: "Joe",  
    age: 21,  
    city: "Bangalore"  
};

document.getElementById("demo").innnerHTML = mySelf; //[object Object]
```

This can however be **maneuvered** and solved with a couple of workarounds:

1. Displaying Object properties by name
2. Displaying Object Properties in a Loop
3. Displaying Object using Object.values()
4. Displaying Object using Object.entries()
5. Displaying Object using JSON.stringify()

## Display the Object Properties

Object properties can be displayed as a string:

```js
// create object
const mySelf = {  
    name: "Joe",  
    age: 21,  
    city: "Bangalore"  
};

// display properties
document.getElementById("demo").innerHTML = mySelf.name + ", " + mySelf.age + ", " + mySelf.city;
```

## Display Object Properties in a Loop

Object properties can also be collected in a loop. 
Here, we use an expression:

```js
// Create an Object
const mySelf = {  
    name: "Joe",  
    age: 21,  
    city: "Bangalore"  
};

// Build a Text
let text = "";
for (let x in mySelf) {  
    text += mySelf[x] + " ";
};

// Display the Text
document.getElementById("demo").innerHTML = text;
```

**NOTE:** You must use `mySelf[x]` in the loop.
`mySelf.x` will not work since `x` is the loop variable.

## Display using Object.values()

`Objects.values()` creates an array from the properties' values.

```js
const mySelf = {  
    name: "Joe",  
    age: 21,  
    city: "Bangalore"  
};

// create array
const myArray = Object.values(mySelf);

// display the array using DOM
document.getElementById("demo").innerHTML = myArray;
```


## Display using Object.entries()

Using `Object.entries()` simplifies using objects in loops:

```js
const pens = {Blue:20, Black:22, Red:10};

let text = "";

for (let [pen, value] of Object.entries(pens)) {  
    text += fruit + ": " + value + "<br>";
}

//display the count of each pen color
document.getElementById("demo").innerHTML = text;
```

## Display using JSON.stringify()

You can convert JavaScript objects into a string with the JSON method `JSON.stringify()`
This method is included in JavaScript and is also supported in most browsers, at least all the major ones.

```js
const mySelf = {  
    name: "Joe",  
    age: 21,  
    city: "Bengaluru"
};

// use JSON.stringify() method
let myString = JSON.stringify(mySelf);

// display the output
document.getElementByID("demo").innerHTML = myString;
```

This method will output a string a string written in JSON notation:

```js
{"name":"Joe", "age":21, "city":"Bangalore"}
```

___

In summary, effectively displaying JavaScript objects in the DOM is crucial for dynamic web development.  
By utilizing techniques such as accessing properties by name, iterating through properties, or using `Object.values()` and `Object.entries()`, you can present object data meaningfully.   

Understanding these methods enhances user experience and showcases JavaScript's versatility in web applications. Mastering these techniques empowers you as a developer to create engaging and dynamic web content.

**Have fun learning 😉**
