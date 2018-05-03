# What is the difference between readdirSync and readdir?

* readdirSync is the synchronous and blocking function that will read the files in the directory provided. readdirSync will not let other functions or simple calls execute until the task of reading files in the directory is complete.

* readdir is an asynchronous and non-blocking function that will read the files in a directory provided. This means that while this function executes it will allow other functions and events to take place before completing its task. This is why it is non-blocking since other functions/events can take place while it is executing. Since this function is asynchronous a callback is required with an error in case something goes wrong and what is to occur upon completion of execution. 

# What is the event loop and how does it handle asynchronous requests?

> The event loop is what allows the single threaded JavaScript to be asynchronous, it is the connection between the callback/event queue and the JavaScript/V8 Chrome stack. **The queue is what process all events and callback functions!** Once your function calls a webapi, the function stays there for the specified timeout that is defined. Once this timeout is up, the callback function is placed in the task queue. The event loop now looks to see if the V8/Chrome stack is empty, if it is the event loop pushes the callback function to the stack to execute. **The main takeaway is the event queue has to wait for the stack to be clear before the event loop pops the function to the end of the stack for execution.**
* Well, we now have the case of 'what if we have a function with a time out of 0?', it still goes to the webapis, and instantly goes into the queue, where the callback WILL WAIT for the stack to be empty before the event loop will push the function to the stack. 

# Given the following code, specify whether the program is asynchronous and non-blocking or synchronous and blocking or synchronous and non-blocking.

```
const fs = require('fs');
const file = fs.readFileSync('foo.txt');
console.log(file.toString());

```
>This is a synchronous and blocking line of code. The readFileSync will block the stack while it is reading the foo.txt file. This will not allow the console.log to execute in the stack until the stack is clear.


# Given the following code, specify whether the program is asynchronous and non-blocking or synchronous and blocking or synchronous and non-blocking. In what order will the console.log statements execute in the code below?

```
const fs = require('fs');
fs.readFile('foo.txt', (err, file) => {
 if (err) throw err;
 console.log(file.toString());
});
console.log("test");

```
>This is an example of an asynchronous and non-blocking function. The readFile will call the API and wait in the event queue for console.log("test") to execute before the callback function console.log(file.toString()) will execute in the stack. 



# In what order will the console.log statements execute in the code below?
```
const fs = require('fs');
fs.readFile('foo.txt', (err, file) => {
 if (err) throw err;
 console.log("A");
 console.log("B")
});
console.log("C");
```
>the readFile is an example of an asynchronous call, thus the console.log("C") will get executed in the stack first. The console.log("A") and console.log("B") will wait in the queue for the stack to be empty. At that point, the event loop will push console.log("A") to execute and then console.log("B") to execute once console.log("A") has executed and the stack is empty.



# setTimeout is a JavaScript function which calls a function after a set amount of milliseconds. Given the following code, explain in what sequence the functions will run and why.
```
function greeting() {
 setTimeout(() => {
   console.log("friend");
 }, 100);
}

function hello(){
 console.log("hello");
}

greeting();
hello();
```
>In this example the greeting function will call the setTimeout() API, and place the callback funciton in the event queue. The hello function will go into the stack and execute first, while the greeting function will wait the queue for the stack to become empty. Once the stack is empty the greeting callback function will execute. 
We will first see hello, then friend.


# Create a function which utilizes a callback. Make sure to add console.log statements to understand when your callback function is called.

>Here is a good example to see that even though the callback function in callbackExample goes to the queue, the console.log outside of the setTimeout runs first, followed by the console.log in the firstInTheRace() function and the two console.log functions in the callback. 

```
function callbackExample() {
	setTimeout(()=> {
	 console.log("I will run third");
	 console.log("I will run fourth");
	},200);
	console.log("I will run first");
}

function firstInTheRace(){
	console.log("I will run second");
}

callbackExample();
firstInTheRace();

Output:

VM964:6 I will run first
VM964:10 I will run second
undefined
VM964:3 I will run third
VM964:4 I will run fourth

```
