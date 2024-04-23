 What is Recursion in JavaScript

 In this example we will be implementing a number decrement counter which decrements the value by one and prints all the numbers in a decreasing order one after another.
 ```<script>
	let decrementCounter = (number) => {

		if(number === 0) return ; 
		console.log(number);
		decrementCounter(number - 1);
	}
	decrementCounter(5);
</script>
```
 In this example, we will be developing a code that will help us to check whether the integer we have passed is Even or Odd. By continuously subtracting 2 from a number, the result would be either 0 or 1. So if it is 0 then our number is Even otherwise it is Odd.
 ```
 <script>
	let checkNumber = (number) => {

		if(number === 0) return (number + " is even");
		if(number === 1) return (number + " is odd");
		return checkNumber(number - 2);
	}
	console.log(checkNumber(5));
	console.log(checkNumber(10));
	console.log(checkNumber(13333));
</script>
```

What is Closure in JavaScript

A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

Consider the following example code:
```
function makeFunc() {
  const name = "Mozilla";
  function displayName() {
    console.log(name);
  }
  return displayName;
}

const myFunc = makeFunc();
myFunc();
```
Here's a slightly more interesting example—a makeAdder function
```
function makeAdder(x) {
  return function (y) {
    return x + y;
  };
}

const add5 = makeAdder(5);
const add10 = makeAdder(10);

console.log(add5(2)); // 7
console.log(add10(2)); // 12
```