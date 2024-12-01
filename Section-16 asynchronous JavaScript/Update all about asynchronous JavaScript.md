# Asynchronous vs Synchronous!

**What is Asynchronous code?**

Imagine you're ordering a pizza. You place your order, and instead of waiting for the pizza to arrive, you continue doing other things - maybe watching TV or reading a book. When the pizza is ready, the delivery person arrives, and you get your pizza.

This is similar to how asynchronous JavaScript works. Instead of waiting for a task to finish before moving on to the next one, JavaScript can start a task and then move on to other tasks. When the first task is complete, the JavaScript engine will handle it, often by calling a function to process the result.

Why Asynchronous JavaScript?

1. Non-blocking operations: Prevents the main thread from being blocked, making your applications more responsive.
2. Efficient resource utilization: Allows the JavaScript engine to handle multiple tasks concurrently.
3. Better user experience: Ensures smoother and faster applications, especially when dealing with network requests or time-consuming operations.

**How Asynchronous JavaScript Works:**
JavaScript uses a mechanism called the event loop to manage asynchronous operations. Here's a simplified overview:

- Task Queue: Asynchronous tasks, like network requests or timeouts, are added to a task queue.
- Event Loop: The event loop continuously checks the task queue.
- Execution: When the main thread is idle, the event loop takes the next task from the queue and executes it.
- Callback Function: The completed task triggers a callback function, which is the code that handles the result of the asynchronous operation.

**Common Asynchronous Patterns:**

1. Callbacks: A function passed as an argument to another function to be executed when the asynchronous operation is complete.
2. Promises: A more structured way to handle asynchronous operations, representing the eventual completion (or failure) of an asynchronous operation and its resulting value.
3. Async/Await: A syntax that makes asynchronous code look more synchronous, making it easier to read and write.

# What is Synchronous javaScript?

Imagine you're waiting in line at a single-teller bank. Each customer has to wait for the teller to finish their transaction before they can be served. This is similar to how synchronous JavaScript works.

In synchronous JavaScript, tasks are executed one after the other, in a sequential manner. If one task takes a long time, the next task has to wait until the first one is finished. This can lead to performance issues, especially when dealing with time-consuming operations like network requests or file I/O.

**Why Avoid Synchronous JavaScript in Certain Scenarios?**

1. Blocking operations: Long-running tasks can block the main thread, making your application unresponsive.
2. Inefficient resource utilization: The JavaScript engine can't handle other tasks while one task is in progress.
3. Poor user experience: Users may experience delays and slow performance.

**When to Use Synchronous JavaScript:**

While asynchronous JavaScript is generally preferred, there are situations where synchronous code can be more appropriate:

- Simple, short-lived tasks: For tasks that don't involve significant delays or external operations, synchronous code can be simpler to write and understand.
- Specific use cases: Certain libraries or frameworks may require synchronous code for specific functionalities.
  In conclusion, while synchronous JavaScript is straightforward, it's important to be mindful of its limitations and choose the right approach for your specific use case. In most modern web development scenarios, asynchronous JavaScript is the preferred method for building responsive and efficient applications.

# AJAX Calls :

AJAX calls are the most important use case of asynchronous javaScript and so let's see what AJAX is all about

AJAX stands for Asynchronous JavaScript And XML: Allows us to communicate with remote web services in an asynchronous way.
with AJAX calls, we can request dada from web services dynamically

**How AJAX works?**

Let's consider our application is running in the browser or client and we want the application to get some data
from a web server.

so with AJAX we can do an HTTP request to the server which has this data and the server will set back a response containing that data that we requested
and this back and forth between Client and server all happens asynchronously in the background, and there can even be different types of requests
like get requests to receive data or post requests to send data to a server and more types of requests that we will cover them all.
Now when wre're asking a server to send us some data this server usually contains a web API and this API is the one that has the data
that we're asking for.
So an API is something pretty important and so let's see what an API and web APIs actually are.

# What is API?

API stands for Application Programming Interface: In general terms and on the very high level of obstruction API is  
a piece of software that can be used by another piece of software, in order ot allow applications to talk to each other
and that's true not only for web development and JavaScript, but for programming in general.

In JavaScript and web development there are countless types of APIs like DOM API or Geolocation API, so these are called APIs because they are a self-contained piece of software
that allow other pieces of software to interact with them, Also we can always implement a small and simple API in a class where we make some methods available as a public interface.
objects made from a class can be seen as self-contained encapsulated pieces of software that other pieces of software can interact with and so that fits the definition of API.
But now let's talk bout the important type of API that we are actually interested in when we use AJAX,
and that are APIs that I like to call Online APIs.
So an online API is essentially an application running on a web server which receives requests for data then retrieves this data from some database and then sends it back to the client

# API data formats:

AJAX stands for Asynchronous JavaScript And XML,
so the **X** there stands for **XML** and XML is a data format which used to be widely used to transmit data on the web.
However these days basically no API uses XML data anymore, the term AJAX is just an old name that got very popular back in the day and so it's still used today,
even though we don't use XML anymore,
So instead most APIs these days use the **JSON** data format, so **JSON** is the most popular data format today because it's just JavaScript object but converted to a string
and therefore it's very easy to send across the web and also to use in JavaScript once the data arrives
