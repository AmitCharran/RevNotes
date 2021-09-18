# JavaScript

## Language Fundamentals

### Basic

* What is JavaScript? What do we use it for?
  * JavaScript is  a programming language that uses Just-in-Time compilation, it conforms to the ECMAScript specifications, and it's used to make interactive web pages.
    * JIT involves compilation during the execution of a program
      * Combination of Interpreted languages and compilation languages
  * Along side HTML and CSS, JavaScript is used to make interactive web pages. HTML and CSS gives structure and JavaScript is responsible for making functionality of those web pages
  
* Can we run JavaScript in a web browser, on a server, or both?

  * You can run it on both. 
    * Browsers have JavaScript built into them
    * To run on server you can use node

* What are the benefits of JS over your core language? Drawbacks?

  * Benefits
    * Speed - code can be run within browsers
    * Popularity - it is used everywhere on the web
    * Ability to create amazing interfaces
  * Drawbacks
    * Client-Side Security - because the code executes on users' computer, it can be easily exploited by looking at the source code
    * Browser Support - Different Browsers interpret JavaScript differently. So you need to write cross-browser code.

* What programming paradigm(s) does JS support?

  * Functional Programming
  * Object Oriented Programming

* What are the data types in JS?	

  * * strings
  * * number
    * booleans
    * undefined
    * null
  * What is the type of NaN? What is the isNaN function?
    * NaN = Not a Number
    * isNaN() function =  checks if a given value is an illegal number or not
  * What is the data type of a function?
    * functions do not have data types
    * But you can apply the typeof operator to those functions and it will tell you the data type of what should be returned
  * What about an array?
    * Object
  * What is the difference between undefined and null?
    * undefined is a type
      * variable was declared but no value was given
    * null is an object
      * you have to assign null in JavaScript

* What are JS objects? what is the syntax?

  * A JS Object has a collection of properties and a property is associated with a name and value

    * A property can also be a function. But in that case it would be called a method

  * Syntax

    * ```javascript
      var car = {
      	make: 'Ford',
      	model: 'Mustang',
      	year: 1969,
          methodName: function(){},
          methodName2: function(){}
      };
      ```

    * 

* Use the object literal syntax to create an object with some properties

  * Above ^

* What are arrays in JS? can you change their size?

  * Ordered list of values
    * It can hold any type
    * Size is auto growing
      * it is possible to create an array with an initial size

* List some array methods and explain how they work.

  * sort 
  * forEach
  * push -- add to end
  * pop -- remove from end
  * splice - remove and return item at an index position -- arr.splice(pos, n) --> n is number of times it should be removed
  * slice -- returns a shallow copy of the array

* What is JSON? Is it different from JS objects?

  * JavaScript Object Notation
    * text-based format to represent structured data. It's commonly used in web applications to transmit data
  * Differences
    * Keys in JSON are in double quotes
    * JSON does not require actual types. Everything is represented as a string
    * JS Object values needs to be a type

* What are some ways you can use functions in JS?

  * You call the function by name and pass parameters
  * You can store the function and definition in a variable

* What are the different scopes of variables in JS?

  * What are the different ways to declare global variables?
    * variable declared outside a function
  * Is it a best practice to use global variables? Why or why not?
    * No
      * if you have a global variables. Scripts after that include variable of the same name will override my previous one
  
* What are some methods on the function prototype?

  * function.prototype.arguments - returns array of the arguments
  * caller - specifies the function that invoked the currently executing function
  * displayName - display name of function
  * length - specifies the number of arguments expected by the function
  * name = the name of function

* If you declare a variable `var` inside a for loop is that block scoped or function scoped?

  * Var is function scoped
  
* If you declare a variable `let` inside a for loop is that block scoped or function scoped?

  * Let is blocked cope

* What will happen?

```javascript
const hi; // Compile Error here, const must be initialized
hi = 3;
console.log(hi);
```

* What are callback functions? What about self-invoking functions?

  * callbacks : A function passed into another function as an argument and invoked inside the outer function

    * They are used to continue code execution after an async operation has completed -- these callbacks are async

  * Self-invoking functions - a nameless function that is immediately invoked after its definition

    * ```javascript
      (function(){
      	console.log("Hello");
      })();
      ```

    * ```javascript
      (function(x){
      	console.log(x);
      })("Hello");
      ```

    * 

* What is a truthy or falsy value? List the falsy values.

  * truthy values -- values that are always true
  * falsy values -- values that are always false
    * false
    * 0
    * -0
    * 0n
    * "",'',``
    * null
    * undefined
    * NaN
    * document.all

* What prints?:

```javascript
let x = 5;
while(x) {
  x--;
  console.log(x);
}// 4 3 2 1 0
```

* What is the difference between == and ===? Which one allows for type coercion?
  * == is loose comparison. 
    * compares two values but ignore datatypes
    * performs a conversion to check equality
  * === is strict comparison
    * campares and checks data types
* What is the difference between `for of` and `for in`?
  * for of - prints values
  * for in - prints names/key/index
* What does the following code do?

```javascript
function addOne(value) {
    value + 1;
}

let x = 5;
addOne(x);
console.log(x); // 5 -- there is no assignment or return value
```

What about this?

```javascript
function changeUsername(user) {
    user.username = 'new-username';
}

let user = {
    username: 'first-username'
};

changeUsername(user);
console.log(user.username); //new-username
```

Why?

* What is the difference between a do-while and a while loop?
  * do-while performs statement and then checks the condition
  * while - checks condition and then performs statement
* What does this do?

```javascript
for(;;){
    console.log('a');
} // a for loop with no conditions, so it will print forever
```

* What is fall-through with regard to switch statements?
  * There is no break. Where ever the switch statement is true. That statement will execute and all following statements will execute.
* What is the difference between `console.log(++x)` and `console.log(x++)`?
  * ++x = pre-increment - it will increment x and then the log statement will execute
  * x++ = post-increment, console log will execute and then x will increment
* Explain what “strict mode” does   
  * Entering strict mode adds severala changes to JavaScript Semantics. Opts in to a restricted variant of JavaScript
    * Prohibits syntax likely to be defined in future versions
  * To enter strict mode
    * `'use strict';`
* What are the naming conventions for a variable used in JavaScript?
  * must begin with letter, underscore, or dollar
  * variables can only contain letters, numbers, underscore, or dollar signs
  * variable names are case sensitive
  * certain words may not be used. Those are reserved words
* What are the naming conventions for a function used in JavaScript?
  * case-sensitive
  * 

### Intermediate

* What is function and variable hoisting?

  * variables can be declared after it has been used

  * ```javascript
    x = 5;
    console.log(x);
    var x; // declared here
    ```

  * var is hoisted and initialize

  * let and const is hoisted but not initialized

* What is closure and when should you use it?

  * Inner and outer function
    * Inner function's scope gets access to outer functions variables

* What does the following code do?

```javascript
let arr = [1, 2, 3, 4];
let x = arr.forEach(function(x){
    return x*x;
});
console.log(x);
```

*prints*: undefined

* What does the following code do?

```javascript
let arr = [1, 2, 3, 4];
let x = arr.map(function(x){
    return x*x;
});
console.log(x);
```

*prints* [1, 4, 9, 16]

* What does the "this" keyword refer to?
  * The current object it belongs to
    * In function "this" is the global object
    * In method "this" is the owner of the method, or current object
* Explain the concept of lexical scope
  * A lexical scope in JavaScript means that a variable defined outside a function can be accessible inside another function defined after the variable declaration. But the opposite is not true; the variables defined inside a function will not be accessible outside that function.
* Explain how inheritance works in JS
  * Prototypal inheritance
    * Each object has a private property which holds a link to another object called prototype
* How would you rewrite this using an anonymous function? Arrow function?
```JavaScript
function hello(){
  console.log('hello');
}
document.getElementById('hi').addEventListener(hello);

() => {console.log('hello');}
```

* What is the difference between `setInterval()` and `setTimeout()`?
  * How would you stop a `setInterval()` once it has been set?
    * setInterval -- performs function/callback every X milliseconds
      * `setInterval(function(){alert('Hello');}, 3000);`
    * setTimeout - lets a function wait on a timer then it will execute
  * Advanced: How do they work with regards to the callback queue?
    * They place function in the V8 stack, where they will execute and then after execution they will go to a queue to return
  
* How would you handle an error in JS?

  * try, catch, finally block

* What attributes does an Error object have?

  * attributes = member fields?
  * message
  * fileName
  * lineNumber

* What is an Immediately Invoked Function Expression?

  * Function that is run as soon it is defined

  * How would you write one?

    * ```javascript
      (function(){
          statement
      })();
      ```

### Advanced

* What are some characteristics of the functional programming paradigms
  * Modularity -breaking things down smaller and smaller part or independent unit
  * State does not exist
  * Low Importance of order of execution
  * Functions can execute in any order
* What does it mean for a function to have no side effects? (what is a pure function?)
  * pure function --> given same input, returns same argument value, Does not modify argument
  * side-effect means change in some sort of state
  * 
* What are the advantages to using a functional approach? (as opposed to OOP)
  * You do not need to keep track of states manually
  * easier to emulate real-world processes.
* Explain how the guard and default operators work
* What happens:
```JavaScript
let h = 'hello';
function process(input) {
  return input || 'goodbye';
}
console.log(process(h)); // hello
console.log(process()); // goodbye
```

### Bonus

* What will happen when I try to run this code: console.log(0.1+0.2==0.3) ?

* What happens?

```javascript
h = 3;
function hello(){
    h = 6;
}
hello();
console.log(h)
```

* What prints?

```javascript
let x = 5;
let b = 2;
for(let i = 0; i < 5; i++) {
    b = b + 1;
}
if(b = x) {
    console.log(b);
} else {
    console.log('Oh no. :(');
}
```



## ES6+

### Basic

* What standard is JS based off of?
  * EcmaScript - general purpose programming language
* What is the difference between var, let, and const keywords?
  * var - globally or functionally scoped
  * let - block scoped
  * const - block scoped and immutable
* How would we rewrite this code with a template literal?

```JavaScript
let n = 'Dorian';
let message = 'My name is '+n;
console.log(message);
let message = `MY name is ${n}`;
```

* What will print:

```JavaScript
let arr = ['chicken', 'pig', 'cow'];
for(let i in arr) {
  console.log(i);// 0, 1 ,2
}
for(let i of arr) {
  console.log(i);// chicken...
}
```

* What will happen:

```JavaScript
let arr = ['chicken', 'pig', 'cow'];
for(const i in arr) {
  console.log(i); // 0, 1, 2
}
```

### Intermediate
* What’s the difference between a normal function declaration and an arrow function?

  * arrow function does not define it's own execution context so it does not have a "this". It's always the outer function or global
  * arrow function cannot be used as a constructor
  * no arguments defined in arrow function.
  * arrow functions can have implicit returns
    * `const increment = (num) => num + 1;`
  * You can create methods with arrow functions. This allows those methods to be used as callbacks easily 

* Does JS have classes? How does this relate to Prototypal inheritance in JS/What is the difference between a Prototype and a Class?

  * No classes, just objects that act like classes
  * Prototypal inheritance allows for objects to reuse properties of another object

* How would you set default values for parameters to a function?

  * ```javascript
    function miltiply(a, b = 1){
        return a*b;
    }
    ```

  * 

* What’s the benefit of computed property names?

  * ```javascript
    const fieldNumber = 3
    
    const myObject = {
      field1: 5,
      field2: 10,
      [`field${fieldNumber}`]: 15 // here is computed property name
        // benefit -- dynamically determine name of the key/name for property
    }
    
    console.log(myObject.field3) // prints 15
    ```

  * 

* Explain the async/await keywords. Why is it preferred to use this instead of .then() methods?

  * Async -- put in front of a function declaration to turn it into an async function

    * ```javascript
      async function hello() {return 'Hello';};
      hello(); //invoking the function now returns a promise
      
      
      let hello = async () => "Hello"; // can use with arrow function
      ```

  * then()

    * ```javascript
      hello().then((value) => console.log(value));
      ```

  * Await

    * Only works inside async functions 

    * can be put in front od any async promise-based function to pause your code on that line until the promise fulfills. Then returns the resulting value

    * ```javascript
      async function hello() {
        return greeting = await Promise.resolve("Hello");
      };
      
      hello().then(alert);
      ```

* How could you make the program print out the statements in order?

```JavaScript
function getData(){
  console.log("2. Getting data from internet, please wait.")
  return setTimeout(function(){
    console.log("3. Returning data from internet after 1000 milliseconds.")
    return [{name: "Avi"}, {name: "Grace"}]
  }, 1000)
}

function main(){
  console.log("1. Starting Script")
  const data = getData()
  //use a timeout promise
  async function waitingASecond(){
     const timeout = timeoutPromise(1000);
      
     await timeout;
  }
  waitingASecond();
  console.log(`4. Data is currently ${data}`)
  console.log("5. Script Ended")    
}

main();
```

Solution:

```JavaScript
function getData(){
  console.log("2. Getting data from internet, please wait.")
  return new Promise(function(resolve){
    setTimeout(function(){
      console.log("3. Returning data from internet.")
      resolve([{name: "Avi"}, {name: "Grace"}])
    }, 1000)
  })
}

async function main(){
  console.log("1. Starting Script")
  const data = await getData()
  console.log(`4. Data is currently ${JSON.stringify(data)}`)
  console.log("5. Script Ended")
}

main()
```

* How do you interact with a Promise? When would it be appropriate to use a Promise?
  * Appropriate to use promise for asynchronous operations
  * Interact with a promise by storing it in a variable
* Write a method that would print to the console the value returned by the promise?
```JavaScript
function helloPromise() {
  let p = new Promise();

  setTimeout(p.resolve(`Hello World`), 500);

  return p;
}
```

Solution:

```JavaScript
helloPromise().then(r -> console.log(r));
```

* Convert this function to use named parameters?

```JavaScript
function add(x, y) {
  return x + y;
}
```

Solution:

```JavaScript
function add(options) {
  return options.x + options.y;
}
```

### Advanced

* What is a Symbol?  What is the advantage using Symbol?
  * A primitive data type in JavaScript. 
  * create by calling `Symbol()`
  * Used to identify object properties
* How could you reference this module in your code?

```JavaScript

export const qcScore = `RED`;

```
Solution:

```JavaScript

import {qcScore} from './filenameTheyShouldAskForFromQC.js';

```

* What is object and array destructuring? Give me an example using the rest/spread operator?

  * Extract properties from objects and bind them to variables

  * ```javascript
    const hero = {
      name: 'Batman',
      realName: 'Bruce Wayne'
    };
    
    const { name, realName } = hero;
    
    name;     // => 'Batman',
    realName; // => 'Bruce Wayne'
    
    
    const name     = hero.name;
    const realName = hero.realName;
    
    // is equivalent to:
    
    const { name, realName } = hero;
    ```

  * Spread operator `...Name`

* What is a generator function? What’s the point of the yield keyword?

  * Generator functions - are functions that can be exited and re-entered
    * typically used with async programming
    * identified by `function*`
  * `yield` - holds the value you need upon return

* What built-in advanced objects does JavaScript provide?

  * 

* What will this print?

```JavaScript

let fname = "Bobbert";
let lname = "Bobbertson";
let role = "manager";
let status = "active";

let user = {
  fname,
  lname,
  [role]: status,
  fullname: () => `${fname} ${lname}`
};

console.log(user);

console.log(user.fullname());

```

## DOM Manipulation

* Explain the following code:

```javascript
document.getElementById("myid").addEventListener('click', (e) => {
  e.stopPropagation(); //stopping the bubbling phase, so if this has a click instance, won't happen
    // need preventDefault() to prevent default behavior
});
```

* What is the global object in client-side JavaScript? What are some built-in functions on this object?
* functions 
  * eval() - evaluate expression, takes string
  * isNAN

**example answers**: `window` is the correct answer (document is a field on the window object), but `document` is also acceptable.

* What is the DOM? How is it represented as a data structure? What object in a browser environment allows us to interact with the DOM?
  * DOM = Document Object Model -- representation of objects that comprises the structure and content on the web. It represents a page, so a program can change it's data structure
  * Data structure is represented as a tree. There's the root, body, head...
  * **Documnet** object allows us to interact with the dom
* List some ways of querying the DOM for elements
  * document.getElementByID
  * document.getElementByTagName
  * document.getElementByClassName
  * 
* How would you insert a new element into the DOM?
  * create an element with `const ele = document.createElement("p");`
  * create text node - `const node = document.createTextNode("This is a new paragraph.");`
  * `ele.append(node)`
  * retrieve a <div> with getElementByID and append to it
  * ***So just append to a div
* What are event listeners? What are some events we can listen for? What are some different ways of setting event listeners?
  * procedures/functions that wait for an event to occur
  * events
    * click
    * keypress
    * keydown
    * keyup
    * mouseleave
    * mouseenter
  * Settle/ handle event listeners
    * prevent default -- stopping page from reloading
    * stop propagation -- 
* What is bubbling and capturing and what is the difference?
  * Bubbling - **When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.**
  * Capturing --  the event goes down to the element.
* What are some methods on the event object and what do they do?
  * event.preventDefault() - cancels the event
  * stopPropagation -
  * StopImmediateProp -- prevents all other listerners from being called
  * composedPath - returns event path (tree nodes)
* Why is `Hello` not visible on the page after calling this function?

```JavaScript
function addElementToBody() {
  let body = document.getElementsByTagName('body');
  body.innerHTML = '<p>Hello</p>';
}
```

**answer:** You can't append a child to an `htmlCollection`.

### Bonus

* What happens?

```javascript
location = 'www.google.com';
console.log(location);
```

## Asynchronous Web

* What is AJAX? why do we use it? What are the benefits of using AJAX? Are there any downsides of using AJAX?

  * AJAX - Asynchronous Javascript and XML
    * Usesbuilt-in XMLHttpRequests(to request data from server) object and Javascript DOM (to display or use data)
  * Benefits - improved user experience
    * Asyn processing
    * multibrowser support
  * Drawbacks
    * dependency of javascript - b/c different browser implement JavaScript differently
    * web pages are difficult to debug and they are prone to potential security threats

* Explain why it is important that AJAX is asynchronous

  * Improve the speed and make everything looks like it's running seemlessly
    * On a web page, when you do something. The page doesn't stop, it continues.  That's because it's asynchonous

* List the steps to sending an AJAX request

  * ```javascript
    const Http = new XMLHttpRequest(); // 1 create XMLHttpRequest
    const url='http://yourdomain.com/'; //2 get your URL 
    Http.open("GET", url); //3 Http.open("GET", url)
    Http.send(); //4 Http.send
    Http.onreadystatechange=(e)=>{ //5 Http.onreadyStatechange
    console.log(Http.responseText) // access info with Http.responseText
    }
    ```

* What are steps to sending an AJAX request?

  * ```javascript
    var xhr = new XMLHttpRequest(); // create XMLHttpRequest
    xhr.open("POST", '/submit', true); // open
    xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
    xhr.onreadystatechange = function() {
        if (this.readyState === XMLHttpRequest.DONE && this.status === 200) {
            // Request finished. Do processing here.
        }
    }
    xhr.send("name=Ketan&id=1");
    ```

  * 

* List the different ready states of the XmlHttpRequest object

  * 0 UNSENT
  * 1 OPENED
  * 2 HEADER_RECIEVED
  * 3 LOADING
  * 4 DONE

* How would retrieve JSON data from an AJAX request?

  * `setRequestHeader("Content-Type", "JSON")`

* How do you handle a failed request in AJAX?

  * 

* What is the Fetch API?

  * Fetch provides generic definition for request and Response object

* How do you send a Fetch request?

  * ```javascript
    fetch('https://www.yourdomain.com', {
            method: 'get'
        })
        .then(response => response.json())
        .then(jsonData => console.log(jsonData))
        .catch(err => {
                //error block
            }
    ```

  * 

* What is the difference between Fetch and AJAX?

  * Fetch is flexible and easy to use
  * Fetch is supported by all modern libraries
  * Fetch doesn't send cookie by default

* How would you retreive JSON data from a Fetch request?

  * `.then(response => response.json)`

* How do you handle a failed request in Fetch?

  * `.catch(function())`

### Bonus

* How would you retrieve XML data from an xhr object?

