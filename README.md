# Interview Preperation Day 2

## Q1. What is execution context

Execution Context is describing the internal working of JavaScript Code. In JavaScript, the environment that enables the JavaScript code to be executed is what we call JavaScript Execution Context.

## Q2. What is an event loop and call stack

Event Loop - The Event Loop is used to monitor the Call Stack and the Callback Queue. If the Call Stack is empty, the Event Loop will take the first event from the queue and will push it to the Call Stack, which effectively runs it.

Call Stack - A Call stack is a queue of tasks, where all the javascript code will execute. Call Stack Follow First
In First Out.

## Q3. What is creation phase and execution phase?

Creation Phase - In this phase, JavaScript allots memory to variables and functions for execution. The JavaScript engine creates the execution context and sets up the script's environment. It determines the values of variables and functions and sets up the scope chain for the execution context.

Execution Phase - In this phase, the JavaScript engine executes the code in the execution context. It processes any statements or expressions in the script and evaluates any function calls.

## Q4. What is the spread operator?
The JavaScript spread operator ( ... ) allows us to quickly copy all or part of an existing array or object into another array or object.
Spread operator allows us to destructure the non-primitive datatype like object and array to access elemnets individually.

    Example:
    let a = [1,2,3];
    let b = [4,5,6];
    let c = [...a,...b]
    console.log(c); //[ 1, 2, 3, 4, 5, 6 ]


## Q5. What is the use of setTimeout
The setTimeout() method sets a timer which executes a function or specified piece of code once the timer expires. It is used to delay the output with given time.

    Example:
    setTimeout(() =>{
    console.log("Displayed after 2 seconds!!!")
    },2000)

## Q6. What are callbacks?
A callback is a function that passed as an argument to another function. It is called when that function completes its task. Callback functions are commonly used in asynchronous programming to handle the results of a task that may take some time to complete.

    Example:
    function Sum(a, b, callback){
    const Add = a + b;
    callback(Add);
    }
    function printResult(output){
    console.log(`Sum is: ${output}`); //Sum is: 15
    }
    Sum(5, 10, printResult)
## Q7. What is callback hell
Callback Hell is essentially nested callbacks stacked below one another forming a pyramid structure. This phenomenon happens when we nest multiple callbacks within a function. The shape of the resulting code structure resembles a pyramid and hence callback hell is also called the “pyramid of the doom”. . It makes the code very difficult to understand and maintain.


    Example:
    function callbackHell() {
        setTimeout(() => {
            console.log("1");
            setTimeout(() => {
                console.log("2");
                setTimeout(() => {
                    console.log("3");
                    setTimeout(() => {
                        console.log("4");
                        setTimeout(() => {
                            console.log("5");
                        }, 5000);
                    }, 4000);
                }, 3000);
            }, 2000);
        }, 1000);
    }

## Q8. Difference between undefined vs not defined vs NaN
1. undefine - This error is caused when the variable is declared but not initialized.
2. not defined - This error is caused when the variable is not declared.
3. NaN(Not a Number) - This error is caused when we are trying to do some task on something which is supposed to be of Number datatype but instead it gets something else.
##
    Example:
    let a;
    console.log(a); //undefined
    console.log(b); //not defined
    let c=10;
    let d="abc"; 
    console.log(c*d); //NaNs
