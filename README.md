# Javascript_md
# JavaScript

## Reverse an array without using .reverse()
```
function arrayExercise (Arr){
var array = [1, 2, 3, 4, 5];
var output = [];
for (var i = array.length - 1; i >= 0; i--) {
    output.push(array[i]);
}
console.log(output);
}
        OR
var array = [1, 2, 3, 4, 5];
function reverse(arr) {
for (var start = 0, end = array.length - 1; start < end; start++, end--) {
    var temp = array[start];
    array[start] = array[end];
    array[end] = temp;
}
console.log(array);
}
```
## Find the second largest number in an array

```
var array = [10, 5, 8, 20, 3];
var first = -Infinity;
var second = -Infinity;
for (var i = 0; i < array.length; i++) {
    if (array[i] > first) {
        second = first;
        first = array[i];
    } else if (array[i] > second && array[i] !== first) {
        second = array[i];
    }
}
console.log("Second largest number is:", second);
```

## Remove duplicates from an array
```
var arr =[1,2,3,3,4,5,5,6,10,10];
const removeDuplicate = (array)=> {
    return [...new Set (array)]
}
console.log (removeDuplicate(arr))
```

## Group array items by a property (e.g., group people by age)
```

const people = [
  { name: "Ram", age: 21 },
  { name: "Hari", age: 25 },
  { name: "Carlos", age: 21 },
  { name: "Diya", age: 25 },
  { name: "Ayush", age: 30 }
];
const groupedByAge = people.reduce((group, person) => {
  const age = person.age;
  if (!group[age]) {
    group[age] = [];
  }
  group[age].push(person);
  return group;
}, {});
```

## Explain and create a closure
```
function outerFunction (){
    const outerVariable = "It is outerFunction ";
    function innerFunction (){
        console.log(outerVariable);
    }
    return innerFunction;
}
    const resultFunction = outerFunction();
    resultFunction();
```

## Create a function that returns a counter

```
function createCounter(n) {
	
	let count = n-1;
	function counter(){	
	return count+=1 ;
	}
	return counter;
}
const counter = createCounter(10);
console.log(counter());
console.log(counter());
console.log(counter());
const secondCounter = createCounter(42);
console.log(secondCounter());
console.log(secondCounter());
```

## Factorial using recursion

```
 function factorial (n) {
    if (n===0 || n === 1){
        return 1 ;
}
return n * (factorial(n - 1));
}
console.log(factorial(5));
```
