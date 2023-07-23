# DAY 4: 
## Lesson Summary:
* Hoisting is an english language convention that we have made up to discuss the idea of lexical scope, without thinking about lexical scope
* In this code, if the teacher on line 5 did not host, then line 4 should print out "Kyle". Because there is no teacher as of line 4 and it should go to the outer scope and find the variable from line
  
![m](https://github.com/M-Alsuleibi/Mastering-JavaScript-in-20-Days/assets/73719352/70144c42-f062-4694-9b40-686a23da852d)

 But this code still throws a TDZ error, and the reason it still throws a TDZ error is because lets and consts still hoist.
* But there is a difference between how they hoist. Number one, lets and consts only hoist to a block, whereas vars hoist to a function. But number two, and this is the more important thing, the difference between var and let const is that var, when it creates its variables and has the plan during the compile time for your scope.And it says there's gonna be a variable called teacher in this scope, it also says when the scope starts, initialize it to undefined.
* When let hoists its variables into its block scope it says create a location called teacher, but don't initialize it. It is in an uninitialized state, uninitialized being different than undefined
#### Closure:
* Closure is when a function “remembers” its lexical scope even when the function is executed outside that lexical scope.
* Modules encapsulate data and behavior (methods) together. The state (data) of a module is held by its methods via closure.
# [Coding Exersises](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md):
### ADVANCED SCOPE Questions
QUESTION #1 Explanation :
> The issue with the current output is due to the closure behavior of JavaScript's setTimeout function. When the setTimeout callback function is executed after 100 milliseconds, it accesses the variable `i`, but since the loop has already finished by that time, the value of `i` is now 5
>> I can fix this by using the IIFE, I create a new scope for each iteration of the loop OR simply using`let` instead of `var` to declare `i` . When  using `let`, a new binding for `i` is created for each iteration of the loop

QUESTION #2 Explanation:
> In the current code snippet, a new array array is created in each iteration of the loop, and only the current value of `i` is pushed into the array
>> To fix it, I move the declaration and initialization of the array variable outside the loop
```javascript
let array = [];
for (let i = 0; i < 5; i++) {
   array.push(i);
   console.log("Current array is: ", array)
}

```
QUESTION #3 Explanation :
> The arrow functions inside the loop capture the variable `i` by reference, not by value. As a result, when the functions are executed later in the `forEach` loop, they all see the final value of `i`, which is 5,
>>  I can use the `let` keyword instead of `var` to declare `i`. When  using `let`, a new binding for `i` is created for each iteration of the loop, ensuring that each function captures the correct value of `i` during that iteration. 
### Closure Questions
QUESTION #1
Create a function called privateCounter() that behaves like a private counter. The function should not have any public variables, and the count should only be accessible through a closure. It should have two methods: increment() and getCount(). The increment() method should increment the count, and getCount() should return the current count.

```javascript
function privateCounter() {
  let count = 0; 

  function increment() {
    count++;
  }

  function getCount() {
    return count;
  }

  return {
    increment: increment,
    getCount: getCount
  };
}

// Example 
const counter = privateCounter();
counter.increment();
console.log(counter.getCount()); // prints: 1

```
QUESTION #2
Write a JavaScript function called generateFibonacci(count) that returns a closure. The closure should generate the next number in the Fibonacci sequence each time it is called. The generateFibonacci function should take a parameter count that determines how many times the closure will generate the next number, and it should use recursion for this purpose.
