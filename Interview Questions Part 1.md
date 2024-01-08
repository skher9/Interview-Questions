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

function abc (){
console.log(a,b,c);

    const a = 30;
    let b = 20;
    var c = 10;

}
abc()
What will be the output of the above snippet.

## Answer:

For "Var" the output will be "undefined" as the variable will be hoisted.
But for "Const" and "Let" the output will be "Undefined" but they will be initialized in the temporal dead zone.

The Temporal Dead Zone is term to describe a state where vairiables are in the scope but they are not yet declared.

## Question 6:

What is the purpose of the map function in JavaScript?

## Answer:

The map function in JavaScript is used to transform each element of an array based on a provided function and create a new array with the results.

## Question 7:

Explain the filter function in JavaScript.

## Answer:

The filter function is used to create a new array containing only the elements that satisfy a specified condition. It filters out elements that do not pass the condition.

## Question 8:

How does the reduce function work in JavaScript?

## Answer:

The reduce function is used to accumulate values of an array into a single result. It takes a callback function and an optional initial value. The callback function takes an accumulator and the current element, and it updates the accumulator with each iteration.

## Question 9.

Polyfills for map() function.

## Answer:

Array.prototype.newMap = function(callBack)
{
let temp = [];
for (let i=0;i < this.length; i++)
{
temp.push(callBack(this[i],i,this));
}
return temp;
}

## Question 10.

Polyfills for filter() function.

## Answer:

Array.prototype.newFilter(callBack)
{
let temp = [];

    for (let i=0;i < this.length; i++)
    {
        if (condition)
        {
            temp.push(callBack(this[i],i,this));
        }
    }
    return temp;

}

## Question 11.

Polyfills for reduce() function.

## Answer:

Array.prototype.newReduce(callBack,initialValue)
{
var accumulator
let temp = [];

    for (let i=0;i < this.length; i++)
    {
        if (condition)
        {
            temp.push(callBack(this[i],i,this));
        }
    }
    return temp;

}

## Question 12:

What is the difference between map and forEach?

## Answer:

While both map and forEach iterate over arrays, map creates a new array based on the transformation specified in the callback function, whereas forEach simply performs an action for each element without creating a new array.

## Info:

const Students = [
{name:"Piyush", rollNumber: 31, marks: 80},
{name: "Jenney", rollNumber:15, marks: 69},
{name: "Kaushal",rollNumber:16, marks: 35},
{name: "Dilpreet",rollNumber:7, marks: 55}
]

## Question 13. Return only name of Students in Capital.

## Answer:

const names = Students.map((student)=>{student.name.toUpperCase()})

## Question 14. Return only the details of those who have scored more than 60.

## Answer:

const details = Students.filter((student)=>student.marks>60)

## Question 15. Return details of those who have marks above 60 and roll no. over 15

## Answer:

const details = Students.filter((student)=>student.marks>60 && student.rollNumber > 15)

## Question 16. Calculate the Sum of marks of all students.

## Answer:

const Sum = Students.reduce((total, marks)=>total = total+marks,0)

## Question 17. Return only names of student who scored more than 60.

## Answer:

const names = Students.filter((student)=>student.marks>60).map((student)=>student.name)

## Question 18. Return total marks for students with marks greater than 60 after 20 marks have been added to those who scored less than 60.

const Total = Students.map((student)=>{
if(student.marks<60)
{
student.marks += 20;
}
return student
}).filter((student)=>student.marks>60).reduce((total,marks)=> total = total+ marks)
