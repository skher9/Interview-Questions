## Question 1.

What is Scope? What are different Scopes.

## Answer:

Scope in JavaScript refers to the context in which a variable or function are declared and it also determines the accessibility of the variables and functions during runtime.

Mainly there are two scopes:

Global Scope:

If any of the variable is defined Globally , then it is accessible through out the entire program, including within functions.

Local Scope:

If any of the variable is declared within a block or a function then it is supposed to have a Local / Functional Scope.

## Question 2.

What is variable Shadowing?

## Answer:

Variable Shadowing occurs when a vaiable is declared within a certain scope and has the same name as another variable declared within the outer scope.
So the inner variable will 'Shadow' the outer variable within its scope.

## Question 3.

Variable Declaration using "Var", "Let" and "Const".

## Answer:

"var" can be declared as many times as needed within a scope. But "let" and "const" cannot be re-declared within the same scope.

In terms of "var" and "let" any variable can be declared without any value, but in terms of "const" you have to declare it with any value.

In terms of Re-Initialization "var" and "let" can be re-initialized but again "const" cannot be initialized again.

## Question 4.

Hoisting in JavaScript.

## Answer:

Hoisting is a behaviour in which the variables and function declarations are moved to the top of their scope during compilation phase, before the code is executed. This allows you to use the variables and functions even before declaration.

## Question 5.

Difference between "==" and "===" operators.

## Answer:

When comparing two variables using '==' it converts both the variables to the same type & then comapares them.
But in terms of '===' the variabled have to be of same type to be considerd to be equal.

## Question 6.

Explain Pass_By_Value and Pass_By_Reference .

## Answer:

Pass by value is basically where we send a copy of a varible that needs to be sent. If the sent varaible is modified then the original variable
will have no impact of it.

Pass by reference is basically where we send the address of the original variable instead of a copy. So if the sent varaible is modified the original variable is imapacted as its updated through reference.

## Question 7.

What is IFFE (Immediately Invoked Function Expression).

## Answer:

Immediately invoked function expression is a function that is called as soon as it is defined. It is known as IFFE.

(function()
{
console.log("Inside IFFE")
})();

## Question 8.

Explain Higher Order Functions.

## Answer:

Higher Order Functio is nothing but a function which takes one or more functions as argument or returns a function is called Higher Order Function.

## Question 9.

Explain call(), apply(), bind().

## Answer:

Call, apply and bind all are pre-defined functions is Javascript.

call(): It invokes a function with specific "this" value and individual arguments are passed as comma seperated.

apply(): It is similar to call but the arguments are passed in form of array.

bind(): It creates a new function which specific "this" value. It returns a new function that can be called later.

## Question 10.

Explain Closure in Javascript.

## Answer:

Closure is a concept in javascript in which the inner function has access to lexical scope i.e. its outer function even if the outer function execution is completed.

## Question 11.

What are object prototype?

## Answer:

A prototype is a blueprint of an object which allows you to use properties and methods of another object even though the properties and object are not present in the current object.

## Question 12.

What are callback functions:

## Answer:

The function that can be passed as a argument to another function is called as callback function.

## Question 13.

Explain REST and SPREAD operator.

## Answer:

Rest operator is used to represent multiple no. of arguments in a array in a function or basically to colllect the remanining elements of an array. It is basically used for function parameter to represent an indefinite number of arguments in a array.

Spread operator is used to spread the elements of an array or object into another array or object.

## Question 14.

What are Promises?

## Answer:

Promises is a concept in javascript which is used to handle asynchronous operations in more effecient way.

It has 3 stages:

1. Pending 2. Resolved 3. Rejected.

A promise takes a callback function with two parameters Resolved and Rejected.
We can consume the promise by attaching the .then() and .catch().

If the promise is resolved we resolve it using .then() and if by any means it is rejected with catch the error in .catch().

Promise.all() : It takes array of promises and returns a single promise. If all the promises are resolved then the final promise will be resolved but if any of the promise is rejected the final promise will be rejected. If the array if empty the resulting promise will be fulfilled.

Promise.allSettled() : It takes array of promises and returns a single promise.The resulting promise will be resolved when all the promises are settled doesn't matter the outcome of individual promise.

Promise.any() : It takes array of promises and returns a single promise. If any of the promise is resolved the resulting promise is resolved. But if all the promises in the array are rejected then the resulting promise is rejected.


## Question 15.

What is Memoization?

## Answer:

Memoization is a concept in which a function will return the same output if the same set of inputs is provided. The output is cached in the memory and is returned if the input is same.

## Question 16.

Explain useState() hook in react.

## Answer:

useState is a hook in react which is used to manage a state in functional component. It returns a array with two values: currentValue and a setter function which can be used to update the current value. And it takes initial state as a argument and return the updated state value whenever the setter function is invoked. Also a component is re-rendered everytime the value is updated.

## Question 17.

Explain useEffect() hook in react.

## Answer:

useEffect is a hook in react basically mimics the lifecycle method in react.

It takes two arguments a callback function and a dependancy array.

If the dependancy array is empty the useEffect will behave like a componentDidMount and will be called only after the inital render.

If the dependancy array has a value then useEffect will behave like a componentDidUpdate and will be called after initial render and everytime the value inside the dependancy array is updated.

Also when we return something from useEffect it behaves like a componentDidUnmount.

## Question 18.

Explain useMemo() hook in react.

## Answer:

useMemo hook uses the concept of memiozation. This can be used if there is a big computation for certain set of input , then the function will be implemented once and its output will be cached for the specific set of input. Unless & until the inputs are changed the cached output will be returned.
The dependancy array cannot be empty when we are using the useMemo hook.

useMemo(()=>{},[]);

## Question 19. 

Explain useCallback() hook in react.

## Answer:

useCallback hook uses the concept of memoization again similar to useMemo. This is mainly used when passing a callback function from parent component to child component. It memoization the callback function & prevents the unnecessary re-renders.
If the dependancy array is empty the useCallback will be executed once and if the dependancy array has a value , the useCallback will be executed everytime the value in the array is updated.

useCallback(()=>{},[])

## Question 20. 

Explain useContext() hook in react.

## Answer:

useContext hook in react allows the component to interact with each other without having to pass data through every single component.

## Question 21.

Explain EventLoop.

## Answer:

So basically when we implement any async operation in javascript , their corresponding callbacks are pushed into event queue after the completion. The main job of event loop is to continously check if the call stack is empty and if it is empty the callbacks from event queue are pushed to call stack one by one.

While moving the callbacks from event queue to call stack on basis of priority. The microtasks are given more priority than macrotasks.

Microtasks:

Promises, async-await, .then(), .catch(), .finally().

Macrotasks:

setTimeout , setinterval, userEvents.

## Question 22.

Explain Debouncing.

## Answer:

It is a technique that delays the execution of a function until the user stops performing certain actions for specific period of time.

To implement this we can use a setTimeOut to set a timer that will execute the function after delay period. We can also use clearTimeOut to cancle the timer if the user performs action again before the delay time ends.

## Question 23.

Explain Throttling.

## Answer:

It is a technique that used to control the rate at which a function is executed, it basically limits the function execution to a fixed interval of time.

To implement throttling, we can use a flag variable to track if the function is ready to run or not. So we can use setTimeOut to set a timer that will set the flag after a time interval. you can use if to check if the flag is true and if it is true the function is executed.