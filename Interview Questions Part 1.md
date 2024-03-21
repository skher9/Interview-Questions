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

useMemo(()=>{},[])
