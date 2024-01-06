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
