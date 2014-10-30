# Data Structures and Algorithms JavaScript Edition

### The Good Parts


### Contents

1. Basics
2. Arrays
3. Lists

#  

#### The Basics


<b>Recursion:</b> a programming technique in which a function calls itself.

Example of Recursion

```
function factorial(number) {
  if (number == 1) {
    return number;
  }
  else {
    return number * factorial(number - 1);
  }
}

console.log(factorial(5));
```

This is how recursion works when the argument passed to the function is 5.

```
5 * factorial(4)
5 * 4 * factorial(3)
5 * 4 * 3 * factorial(2)
5 * 4 * 3 * 2 * factorial(1)
5 * 4 * 3 * 2 * 1
5 * 4 * 3 * 2
5 * 4 * 6
5 * 24
120
```
#  

<b>Objects: </b>a collection of properties created by defining a constructor function.
