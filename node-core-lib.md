# Why is the fs core module important for Node development?
> Nodes fs core module allows for a way to access the file system through code, and enables many important tasks to be able to be written for server-side. Tasks such as: making directories, reading directories, creating files, copying files, checking if files exist, reading files and deleting files. This core module provides a lot of functionality for file system management. 

# What is the difference between sync and non-sync methods in the fs module?
>Synchronous methods or blocking methods execute in sequential order, waiting for the line of code to finish executing before moving on to the next line of code.
>Asynchronous or non-blocking means that the code does not wait for the current line to finish executing before moving on to the next line. 

# Why are modules used?
>Modules are used for reusability and to enable functionality through simplicity and ease. Modules are libraries that are imported into a file to enable something in the application. Modules also inspire shareability of code to enable greater collaboration and provide great extensibility for the framework/language.

# Why are libraries such as fs used in Node programming?
>Libraries such as fs are used to enable funtionality that is required for the programming language to be useful. File system accessibility is a huge must for server-side or back-end languages since they are dealing with many I/O functionalities and creating, updating, deleting files. Without libraries such as fs, Node users would not have point of reference to using Node and would have to create and write their own methods of how to do something such as accessing file system functionalities. 



# Create a Github repo called simple-http-node-server. Create an HTTP server on port 3000 with a request handler that creates a file named hello-world.txt. You will be using the fs module to do this. Write the content: "Hello to this great world" to the hello-world.txt file. Please submit your finished code in your submission.


```
const http = require('http');
const fs = require('fs');
const port = 3000;



const requestHandler = (req, res) => {
	res.end(fs.writeFile("/hello-world.txt","Hellow to this great world","utf8",(err) => {
		if(err)throw err;

		console.log('success');
	}));
};

const server = http.createServer(requestHandler);

server.listen(port, (err)=> {
	if(err){
		return console.log(`You have an error: ${err}`);
	}
	console.log(`server is listening on ${port}`)
});

```