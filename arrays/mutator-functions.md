# Mutator Functions

Mutator functions allow us to modify the contents of an array without referencing the individual elemts.

**push( )** adds elements to the end of an array.

**unshift( )** adds elements to the beginning of an array.

```
var numSet = [3,4,5,6];
var newNum = 1;
numSet.unshift(newNum);

console.log(numSet);
```

If we wanted to add elements to the beginning of an array without unshift we could do like so:

```
var numSet = [3,4,5,6];
var newNumSet = 1;
var N = numSet.length;
for(var i = N; i >= 0; i--) {
  numSet[i] = numSet[i - 1];
}
numSet[0] = newNumSet;
console.log(numSet);
```
We would get 1, 3, 4, 5, 6 in return.
