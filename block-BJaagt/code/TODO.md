Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = "Arya";
}
console.log(username); // 'Reference Error username is not defined'
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = "Arya";
}
console.log(username); // Reference Error username is not defined
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the block and we can't access the variable defined inside a block from outside since const is a blocked scoped.

The above code will throw an error `Reference Error username is not defined`.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = "Arya";
}
console.log(username); // Reference Error username is not defined
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the block and we can't access the variable defined inside a block from outside since let is a blocked scoped.

The above code will throw an error `Reference Error username is not defined`.

4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = "Arya";
}
console.log(username); // Arya
```

In above code we are looking for the variable named `username`. The variable is inside the block and we can access the variable defined inside a block from outside since var is function scoped only.

Output will be `Arya`.

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  var username = "Arya";
}
console.log(username); // SyntaxError: Identifier 'username' has already been declared
```

In above code we are looking for the variable named `username`. Initially the variable `username` is declared using let in global scope with value "John" but then it is redeclared to be "Arya" using var which is function scope and since it is insisde blocked it will be declared in global scope but since variable declaration with let can't be redeclared in same scope it will throw an error.
The above code will throw an error `SyntaxError: Identifier 'username' has already been declared`

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  let username = "Arya";
}
console.log(username); // John
```

In above code we are looking for the variable named `username`. Initially the variable `username` is declared using let in global scope with value "John" and `username` variable is again declared to be "Arya" using let so it will create a block scoped and the console.log is in global scope so it will check in global execution context's memory and output will be `John`

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
function sayHello() {
  let username = "Arya";
}
sayHello();
console.log(username); // John
```

In above code we are looking for the variable named `username`. The variable `username` is declared in global scope using let with value "John" and also the variable username is declared in function sayHello.Th e console.log command is in global scope so it will search in Global execution context memory and there the value of variable username is John. So output will be `John`

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, "First");
  /* 0 First
1 First
2 First
3 First
4 First
5 First
6 First
7 First
8 First
9 First*/
}
console.log(i, "Second"); // 10 Second
```

In above code we are looking for the variable named `i`. The variable `i` is declared using var and it is function scope only. initially the for loop will run and value of i will be printed from 0 to 9, after that value of `i` will be 10 then loop will break and its value will be 10 only and output of second console.log will be 10.

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, "First");
  /* 0 First
1 First
2 First
3 First
4 First
5 First
6 First
7 First
8 First
9 First*/
}
console.log(i, "Second"); // ReferenceError: i is not defined
```

In above code we are looking for the variable named `i`. The variable `i` is declared using let and it is blocked scope. initially the for loop will run and value of i will be printed from 0 to 9, after that outside of for loop block value of `i` is not declaration. So it will throw an error `ReferenceError: i is not defined`.
