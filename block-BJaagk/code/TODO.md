1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

//function expression
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
//arrow function
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
//function declaration
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
}; //function expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
}; //function expression
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
}; //function expression
```

```js
let percentage = (marks, total) => (marks * 100) / total; //function expression
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

- Since functions are objects in javascript and objects are non-primitve data types which can be stored in a variable so, function definition is an expression in javascript.
  eg:

```js
let sum = (a, b) => a + b;
```

4. Why is a function call an expression in JavaScript?

- since functions are objects in javascript, and objects can be stored in a variable, so executing a function is like executing an object hence it is an expression in javascript.

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); //Valid
five = add; // valid
five = five(10, 11); // valid
five = function () {
  return "Hello";
}; // valid
```

6. What is the difference between function definition and function call? Explain with an example.

- Function definition defines the series of step of a function. Function call s the execution of that series of function.
  eg:

```js
function isEven(num) {
  return num % 2 === 0;
} //function definition

isEven(4); //function call
```

7. What is the similarities between function definition and function call?

- both are expression in javascript and can be stored in a variable.

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log("Hello World!");
}

hello.user = "Sam"; // valid
```

9. What is higher order function explain with an example.

- A Higher-Order function is a function that receives a function as an argument or returns the function as output.
  eg:

```js
function isEven(num) {
  return num % 2 === 0;
}

function filterEven(arr, fn) {
  return arr.filter((ele) => fn(ele));
} //higher order function
```

10. Explain what is callback function. Why you can pass a function inside a function?

- callback function is a function which is passed as an argument to another function. In javascript since fucntions are objects, so we can pass them as argument for any other function.
