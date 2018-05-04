# How do you access the DevTools for Node in Chrome?
>DevTools for Node in Chrome are accessed through typing chrome://inspect into the browser and clicking on the "Open dedicated DevTools for Node". 

# What are the main differences between the regular Chrome DevTools and the DevTools for Node?
>Regular Chrome DevTools allow for front-end developers to test new features, look at HTML, CSS and JavaScript code in the browser, and see how changing the code effects the web page. You can also see the webpage/webapp hierarchy, look at loading network performance, etc. These tools are mainly used for front-end or client-side development and are simply accessible through right-click and inspect or view->developer->developer tools. 
>Node.js DevTools are dedicated to back-end or server-side code, and specifically designed for Node.js. 

# Using the built-in Node debug tool, what command do you use to continue the execution of your code.
> cont-will continue the execution of code to the breakpoints.


# Which statement do you put in your code to set a breakpoint?
> debugger-will create a breakpoint that will tell chrome devTools the point at which to stop.

> Chromes' Node DevTools seem to be extremely useful in being able to column break as well as row break. This allows to pause inside an asynchronous arrow function to catch exceptions within these functions execution. The ability to Blackbox a script also adds important functionality that hides frames that we do not want to look at, and step into the event handler that is needed to be inspected to find the exception. Live edit is another important feature of the node dedicated chrome DevTools.

some options for debugging scripts:

* process._debugProcess(pid) is really useful to debug an existing node process. 
* terminal debugging through CLI debugger 
* core inspector module-via require('inspector')

>Tracing-anything that is taking time-ability to look at trace. Trace events is now enabled in node. JSON file will be the output, that can be opened in Chrome about:tracing
We can look at V8 execute time, compiling, parsing, etc.
Latencies can also be identified through looking at requests.



