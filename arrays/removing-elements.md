# Removing Elements from an Array

**pop( )** removes elements from the end of an array.

**shift( )** removes elements from the beginning of the array.

Without mutator functions, removing elements form the beginning or an array requires shifting elements toward the beginning of the array.

```
var numSet = [9,1,2,3];

for (var i = 0; i < numSet.length; i++) {
  numSet[i] = numSet[i + 1];
}
```
result: 1, 2, 3, undefined

This would leave us with a last element undefined. With shift this doesn't happen.

```
var numSet = [9,1,2,3];
numSet.shift();
```

result: 1,2,3
