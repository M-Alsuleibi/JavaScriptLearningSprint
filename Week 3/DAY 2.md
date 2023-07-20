# DAY 2: Static Typing And Scope
## Static Typing:
## Lesson Summary:
* There is a problem if you are coding nd not know anything about your types .
* Linting is a tool that applies an opnion about your code and you take a dicision based on this opnion
* Benefits and drawbacks of using tools like TypeScript and Flow for type checking:
  * Benefits:
    1. Catch type-related mistakes
    2. Communicate type intent
    3. Provide IDE feedback
  * Caveats:
    1. Inferencing is best-guess, not a guarantee
    2. Annotations are optional
    3. Any part of the application that isn't typed introduces uncertainty
* Type-Aware Linting in TS:
  * annotating
  * custom types & signatures
  * validating operand types
## STATIC TYPING Coding Exersice:
#### QUESTION #1
Given the following `promisesArray`, convert the array into an object using the
`convertToObj` function.

You should apply typescript types to every promise, the input of `convertToObj`,
and the output of `convertToObj`. 

Build interfaces and types as needed.

```javascript

const sayHelloWorld = new Promise(resolve, reject => {
  resolve("Hello world!");
});

const checkBoolean = (boolean) => new Promise(resolve, reject => {
  if (boolean) {
    resolve(boolean);
  } else {
    reject(`Input is false :(`)
  }
})

const returnObj = new Promise(resolve, reject => {
  resolve({
    x: "meow",
    y: 45,
  })
})

const promisesArray = [sayHeloWorld, checkBoolean, returnObj];

const convertToObj = (array) => {
  //write your code here;
  return obj;
}

```

## Scope:
Lesson summary:
* Scope: where to look for things
  * Nested Scope
  * Hoisting
  * Closure
  * Modules
* All variable are in one of two roles in program :
 1.Target Reference: receicving the assignment of some value , or
 2. Source Reference: retrieving a value from the variable
*  We have to think about JavaScript as a two-pass system rather than a single-pass(the first pass compilation, second pass execution):
  * What happens when we process our code, is compilation. We are gonna process the code first, and set up the scopes, and then we are gonna execute it
  * So if the identifiers are the marbles, what are the buckets? The buckets are our units of scope. And in JavaScript we primarily have functions, but we also now have blocks.
* Compilation And Scope vs. Executing Code:
   * First pass compilation : There is a compilation time when been a conversation between 'the scope manager' and 'the compiler' . What happened is discriminate each identifier to specific scope accourding where the 'declaration/target ' positioning occured.
   * Second pass execution: there is a runtime after when been a conversation between 'the scope manager' and 'the virtual machine or JS engine'. Here the 'source' been processed.
> **So we discover the source versus target position at compile time, but we don't use that information until run time.**
 
