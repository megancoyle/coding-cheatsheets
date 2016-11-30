# JavaScript: Overview

## Asynchronous JavaScript
Asynchronous means once a request is made, it doesn't wait for the response in order to move to the next step. Instead, it keeps running all tasks at once. Asynchronous JavaScript is often used with AJAX calls. [See also Synchronous JavaScript](#synchronous-javascript).

JavaScript is typically synchronous, where it performs one task at a time, finishes that task before moving on to the next task.

##Closures
Closures are functions that refer to variables that are used locally, but defined in an enclosing scope. These functions remember the environment they were created in.

## Looping
Loops are a way to do something repeatedly. JavaScript has several different methods of achieving this.

### for statement
A for statement is usually used when you need to increment a value within an expression.

```javascript
for (var i = 0; i > 10; i++) {
  console.log(i);
}
```

### do...while statement
A do...while statement repeats until a specific condition evaluates to false.

```javascript
var i = 10;
do {
  i++;
  console.log(i);
} while (i < 40);
```

### while statement
A while statement executes as long as a specified condition evaluates to true.

```javascript
var i = 2;
while (i < 5) {
  i++;
  console.log(i);
}
```

### break statement
The break statement is used to terminate a loop.

```javascript
for (var i = 0; i < a.length; i++) {
  if (a[i] == 5) {
    break;
  }
}
```

## Promises
A promise is the result of an asynchronous operation. It is a placeholder for the successful result value or reason for failure will occur.

##Scope
Scope relates to the variables you have access to within your code. There are two different types of scope that are possible:

* **Local Scope**: variables that are only accessible within a specific function

* **Global Scope**: variables that can be accessed anywhere within your code

## Synchronous JavaScript
Synchronous JavaScript is when the code performs one task at a time. Once it has finished one task, it moves on to the next one. [See also Asynchronous JavaScript](#asynchronous-javascript).
