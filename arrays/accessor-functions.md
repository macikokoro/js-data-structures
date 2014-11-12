# Accessor Functions

JavaScript has built in functions that can be used to access the elements of an array. These accessor functions return some representantion of the target array as the return values.

**indexOf( )** - useful if we need to see if the an argument has been passed to the function is found in the array.

```
var theBat = "Batman";
var n = str.indexOf("a");
```

The result of n would be 2.

If there are multiple occurrences of the same data in an array, **indexOf( )** will return the position of the first occurrence.

A similar function **lastIndexOf( )** will return the position of the last occurrence, or -1 if the argument is not found.
