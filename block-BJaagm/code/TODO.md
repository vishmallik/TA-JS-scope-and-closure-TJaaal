1. What does thread of execution means in JavaScript?

- When we execute a code, javascript engine executes the code line by line. This is known as thread of execution and then gives the output.

2. Where the JavaScript code gets executed?

- Javascript code gets executed in Global Execution context.

3. What does context means in Global Execution Context?

- Context is the environment on which we are executing the code.

4. When do you create a global execution context.

- Whenever JavaScript engine executes a code it creates a Global Execution Context which gets created only once for the whole code.

5. Execution context consists of what all things?

- Execution context consists of a Execution area where code gets executed and a storage area where variable are stored in a memory.

6. What are the different types of execution context?

- There are two types of execution context : a. Global execution context and b. Function execution context.

7. When global and function execution context gets created?

- When JavaScript engine execute a code, Global Execution Context gets created once and then code gets executed in it. And whenever, A function is executed a Function Execution Context gets created and deletes after the execution of function is completed.

8. Function execution gets created during function execution or while declaring a function.

- Function execution context gets created during function execution/call. not while function declaration.

9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.

```js
var user = "Arya";

function sayHello() {
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

![](./img/Screenshot%20from%202022-08-25%2020-54-49.png)

```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount) {
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

![](./img/Screenshot%20from%202022-08-25%2021-18-03.png)

```js
var age = 21;

function customeMessage(userAge) {
  if (userAge > 18) {
    return `You are an adult`;
  } else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](./img/Screenshot%20from%202022-08-25%2021-35-52.png)
