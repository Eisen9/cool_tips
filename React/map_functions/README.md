# Map Function 

## Description
The map function is used to create a new array with the results of calling a provided function on every element in the calling array.

## Syntax
```javascript
let newArray = arr.map(callback(currentValue[, index[, array]]) {
    // return element for newArray, after executing something
}[, thisArg]);
```

## Parameters
- callback: Function that is called for every element of arr. Each time callback executes, the returned value is added to newArray.
    - currentValue: The current element being processed in the array.
    - index (optional): The index of the current element being processed in the array.
    - array (optional): The array map was called upon.  
- thisArg (optional): Value to use as this when executing callback.

## Return value
A new array with each element being the result of the callback function.

## Examples
```javascript
let numbers = [1, 4, 9];
let roots = numbers.map(function(num) {
    return Math.sqrt(num)
});
// roots is now [1, 2, 3]
// numbers is still [1, 4, 9]
```


## Reference
[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

