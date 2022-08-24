1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

let percentage = function percenatge(marks, total) {
  return (marks * 100) / total;
};

let percentage = function (marks, total) {
  return (marks * 100) / total;
};

let percentage = (marks, total) => {
  return (marks * 100) / total;
};

let percentage = (marks, total) => (marks * 100) / total;
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

- since function call always returns a value whether truthy or falsy but it return a value so hence it is an expression in javascript.

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); //Valid since add function will be called and return a value 5
five = add; // valid since we are assigning a function definition to a variable five.
five = five(10, 11); // valid since five is an function expression and initially it will be executed and 21 will be assigned to five variable.
five = function () {
  return "Hello";
}; // valid here five is a varible and function definition is assigned to it so it is valid.
```

6. What is the difference between function definition and function call? Explain with an example.

- Function definition defines the series of step of a function. Function call is the execution of that series of function.
  eg:

```js
function isEven(num) {
  return num % 2 === 0;
} //function definition

isEven(4); //function call
```

7. What is the similarities between function definition and function call?

- both are expression in javascript

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

- callback function is a function which is passed as an argument to another function. In javascript since functions are expressions , so we can pass them as argument for any other function.
