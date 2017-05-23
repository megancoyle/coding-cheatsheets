# General Programming

## Control Structures: Loops
Loops allow us to write code that executes more than once, without having to repeat ourselves.

* while loops
```
while (expression) {
  statement;
}
```
* for loops
```
  for (expression1; expression2; expression3) {
    statement;
  }
```
* foreach loops take an array and loop through each item
```
  foreach (array) {
    statement;
  }
```
for associative arrays:
```
  foreach (array as key => value) {
    statement;
  }
```
* break stops the whole looping process if the loops finds what it's looking for

## Logical Expressions
For controlling the flow of code, where our code makes choices about what should happen based on different conditions.

* if statements
* else and elseif statements
* switch statements (usually used with evaluating the value of strings):
```
  switch (value) {
    case 'case1':
      statement
      break;
    case 'case2':
      statement
      break;
    default:
      statement
      break;
    }
```

## Operators
### Comparison Operators
* equal: ==
* identical: === (same type and value)
* compare: > < >= <= <>
* not equal: !=
* not identical: !==

### Logical Operators
* and: && (both parts must be true)
* or: ||
* not: !
