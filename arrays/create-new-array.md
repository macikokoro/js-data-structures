# Creating New Arrays from Existing Arrays

The two built in methods that allows us to create new arrays form existing arrays are **concat( )** and **splice( )**.

**concat( )** allows for putting together two or more arrays.

```
var looney = ["Bugs", "Daffy"];
var moreLooney = ["Elmer", "Yosemite Sam"];
var looneyGroup = looney.concat(moreLooney);
```

The output values are: Bugs, Daffy, Elmer, Yosemetie Sam

**Splice( )** allows for creating a new array from a subset of an existing array. This method adds new contents while removing existing.

```
var xMen = ["Wolverine", "Xavier"];
xMen.splice(0, 1, "Rouge");
```
This would log Rouge, Xavier because we told it at position 0, add a new item, and remove one item.
