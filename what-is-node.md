# In your own words highlight the differences in functionality and purposes Client-Side and Server-Side code serves in a full-stack web application.

>Client-side code is the front-end code that runs in a browser process. This code renders the views/components of a page, handles user interactions, has ability to interface with HTML and the DOM, and uses script tags to split code into files. Moreover, client-side code uses Asynchronous JavaScript and XML to make HTTP requests to servers(back-end/server-side.)

>Server-side code is the back-end code that runs in a specific engine/runtime process and does not render anything. This is the code that handles the HTTP requests that the client-side code or APIs make and sends back the responses for that code. Server side does not interact with the DOM directly, does not interface with HTML or selectors and uses modules instead of script tags to split code into files. Server-side code can make direct HTTP requests unlike client-side code.

# What explains Nodes' rise in popularity and use? What does "Isomorphic JavaScript programming" mean? Provide some real-world examples not listed in this checkpoint of companies using Node.js.

>Client-side and server-side code traditionally relied on different technologies and languages for implementation. This complicated creating websites/web applications and developers sought after creating a unified language to use for the client-side and server-side. This is where JavaScript excelled, due to its non-blocking and asynchronous nature changing and improving I/O access operations. Languages like PHP and Ruby require events to follow a line of execution, meaning you cannot do anything while you wait for a response, while node js uses stacks and queues to not have to wait for slow I/O or database operations to continue processing. This makes node fast and able to handle millions of concurrent connections at once. 
>Isomorphic JavaScript means using JavaScript on the client-side as well as the server-side. This makes an application unified in design, language and alleviates some issues with separation of concerns. In this scenario, the full-stack web application is built using JavaScript with some kind of RDBMS for storage/retrieval/writing/updating/etc.

### Companies using Node js
	* LinkedIn
	* Trello
	* Walmart
	* Paypal
	* Medium
	* eBay
	* NASA
	* Groupon
	* Lowes

# Draw a diagram of a full-stack web application and its key components.

https://drive.google.com/file/d/1ekzP-0-uXQA5Lf23ZinoKHSjrlV27GRc/view?usp=sharing
