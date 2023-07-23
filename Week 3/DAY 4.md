# DAY 4: 
## Lesson Summary:
* Hoisting is an english language convention that we have made up to discuss the idea of lexical scope, without thinking about lexical scope
* In this code, if the teacher on line 5 did not host, then line 4 should print out "Kyle". Because there is no teacher as of line 4 and it should go to the outer scope and find the variable from line
![m](https://github.com/M-Alsuleibi/Mastering-JavaScript-in-20-Days/assets/73719352/70144c42-f062-4694-9b40-686a23da852d)

 But this code still throws a TDZ error, and the reason it still throws a TDZ error is because lets and consts still hoist.
* But there is a difference between how they hoist. Number one, lets and consts only hoist to a block, whereas vars hoist to a function. But number two, and this is the more important thing, the difference between var and let const is that var, when it creates its variables and has the plan during the compile time for your scope.And it says there's gonna be a variable called teacher in this scope, it also says when the scope starts, initialize it to undefined.
* When let hoists its variables into its block scope it says create a location called teacher, but don't initialize it. It is in an uninitialized state, uninitialized being different than undefined
