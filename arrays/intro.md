# Arrays

Definition: a linear collection of elements which can be accessed via indices.
In JavaScript arrays are objects.

#### Creating Arrays.

Array literal `var numbers = [];`

Array constructor `var numbers = new Array();`

#### Accessing elements of an array sequentially with a for loop.

```
var numbers = [1,2,3,4,5,6];
var sum = 0;
for (var i = 0; i < numbers.length; i++) {
  sum += nmbers[i];
}

console.log(sum);
```

#### Creating Arrays from strings.

Arrays can be created as the result of calling the <b>split( )</b> function on a string. This function breaks the string at a common delimiter, for instance a space for each word. It creates an array consisting of individual parts of the string.

```
var myCatName = "Mr. Spartacus";
var words = myCatName.split(" ");
for (var i = 0; i < words.length; i++) {
  console.log("word " + i + ": " + words[i]);
}
```

The output would be word 0: Mr. and word 1: Spartacus.

If we wanted to assign this string to a new array.

```
var myCatName = "Mr. Spartacus";
var myCatArray = [];
var words = myCatName.split(" ");
for (var i = 0; i < words.length; i++) {
  myCatArray[i] = words[i];
}

console.log(myCatArray);
```
