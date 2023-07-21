# DAY 3: Scope, Function Expressions And Advanced Scope 
# Lesson Summary:
## Function Declaration vs Function Expression:
### Function Declaration:
To declare a function, you use the function keyword and specify a name for the function. For example:
```javascript
function generateIntro(name) {
  return `Hi, my name is ${name}`
}

const dillion = generateIntro("Mohammad")
console.log(dillion)

// Hi, my name is Mohammad
```
### Function Expression:
Here, you create a function expression and assign it to a variable that can be called. You can do this in two ways:
1.  Function Expressions with the function keyword
One way to do this is to use the `function` keyword without a name, which makes it an anonymous function. Here's how:
```javascript
const generateIntro = function(name) {
  return `Hi, my name is ${name}`
}

const dillion = generateIntro("Mohammad")
console.log(dillion)

// Hi, my name is Mohammad
```
2.  Arrow function expressions
You can also create function expressions with arrow functions. Arrow functions, introduced in ES6 allow you to write functions in a short manner.
But arrow functions cannot be declared; they can only be expressed. Here's an example:
```javascript
const generateIntro = (name) => {
  return `Hi, my name is ${name}`
}

const dillion = generateIntro("Mohammad")
console.log(dillion)

// Hi, my name is Mohammad
```
* Named Function Expressions: Benefits
  1. Reliable function self-reference (recursion, etc)
  2. More debuggable stack traces
  3. More self-documenting code 
## Advanced Scope:
* JS is 100% lexically scoped. Lexical scope is the ability for a function scope to access variables from the parent scope. We call the child function to be lexically bound by that of the parent function.
* The principle of least exposure or the principle of least privilege: You should default to keeping everything private, and only exposing the minimal necessary. Three core reasons for this principle:
  1.  We have naming collision problems. And if you hide something within a scope, or hide something on a namespace or do some other sort of hiding, then you reduce the surface area for name collisions.
  2.  If you hide something, it means that somebody else can't accidentally of intentionally misuse that thing.
  3.  You protect yourself for future refactoring. If you expose something, it's a guarantee almost, there's gotta be some CS law for this, it's a guarantee that somebody's gonna use it. And as soon as they start using it, now you are restricted in your ability to freely refactor it.
* [IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)
* Block scope :Blocks are not scopes until they have a `let` or `const` inside of them and then that sort of implicitly makes them a scope.
* When using `const` you can not reassign! BUT you can mutate like in arrays declared with `const` keyword.It prefered to use it with primitive immutable values like strings, numbers, and booleans. 
# [Coding Exercises](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day3-tasks/tasks.md)

#### QUESTION 3 Solution:
> Explanation: . When `inner1()` is called, it accesses the value of `x` from its outer lexical environment, which is `outer1`. Since `x` is defined within `outer1`, `inner1` can access and log the value of `x`, which is `10`.
#### QUESTION 4 Solution:
> Explanation :the `inner2` function creates a new variable named `x` inside its own scope using the `var` keyword. This local variable `x `takes precedence over the outer variable `x` declared in the `outer2` function. When `inner2()` is called, it looks for the variable `x` within its own scope first. Since `x` is declared inside `inner2` with a value of `20`, it logs `20` to the console.
---
**In JavaScript, when a variable is declared within a function, it creates a new variable local to that function, which can shadow (hide) variables with the same name in outer scopes. This concept is known as variable shadowing.**
