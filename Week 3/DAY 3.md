# Scope, Function Expressions And Advanced Scope 
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
