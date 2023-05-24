 # Javascript-Coding-Questions
Javascript (Arrays, Functions)
 ## 1. Write a function that takes an array of numbers as input and returns the sum of all the numbers.
```
function sum(arr){
    let summ = 0;
    // console.log(summ)
    for(let i = 0 ; i<arr.length; i++){
        summ = summ + arr[i];
    }
    return summ;
}
console.log(sum([1,2,3,4]));`

function sumArr(arry){
   const mySum =  arry.reduce((accumulator, currentValue)=>{
        return accumulator + currentValue;
    });
    return mySum;
}
console.log(sumArr([1,2,3,4,5]));
```

 ### What is reduce method?
 The reduce method cycles through each number in the array much like it would in a for-loop.
 The reduce() method executes a reducer function for array element.
The reduce() method returns a single value: the function's accumulated result.
The reduce() method does not execute the function for empty array elements.
The reduce() method does not change the original array.
 The reduce() method takes in:

 callback - The function to execute on each array element (except the first element if no initialValue is provided). It takes in
accumulator - It accumulates the callback's return values.
currentValue - The current element being passed from the array.
 initialValue (optional) - A value that will be passed to callback() on first call. If not provided, the first element acts as the accumulator on the first call and callback() won't execute on it.
Syntax: array.reduce(function(total, currentValue, currentIndex, arr), initialValue)

## Finding Average with the help of reduce method:
```
const euros = [29.76, 41.85, 46.5];

const average = euros.reduce((total, amount, index, array) => {
 total + amount
  if( index === array.length-1) { 
    return total/array.length;
  }else { 
    return total;
  }

});
console.log(average)
```
### The reduce() method takes two arguments: a function and an initial value. The function is called once for each element in the array, and the initial value is used as the first argument to the function. The function returns the accumulated value, which is then used as the first argument to the function for the next element in the array. This process continues until all of the elements in the array have been processed.

## 2. Implement a function that reverses a given string.
```
function reverseString(str) {
  const reversedString = [];
  for (let i = str.length - 1; i >= 0; i--) {
    reversedString.push(str[i]);
  }
  return reversedString.join("");
}
const str = "hello";
const reversedStr = reverseString(str);
console.log(reversedStr); // olleh
```
##### What is push here?
In JavaScript, the push() method is used to add one or more elements to the end of an array. It is a mutating method, which means that it changes the original array. The push() method takes one or more elements as its arguments and adds them to the end of the array. The elements are added in the order that they are specified in the arguments.

##### What is join here?

In JavaScript, the join() method is used to convert an array to a string. The join() method takes a separator string as an argument. The default separator string is a comma.

#### Second Method
```
const str = "Hello, world!";
const reversedStr = str.split("").reverse().join("");
```
##### What is split() here?

The split() method in JavaScript is used to split a string into an array of substrings. The split() method takes a separator string as an argument. The default separator string is a space.

