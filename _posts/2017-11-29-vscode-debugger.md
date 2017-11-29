---
layout: post
title: How to Set up Visual Studio Code to Debug Requests with Node.js
---

You can use Visual Studio's debugging features not just to debug a particular script, but to set breakpoints while your Node.js application is running.

If requests to a given endpoint are not behaving as expected, this is a good way to start fixing the problem.

In this example, I'll assume you are starting your server process with `nodemon`, but the steps are similar if you run the server some other way--just make sure you choose the correct config options.

## Create the Configuration File

Go to the Debug section of Visual Studio.

![debug section]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.57.17 AM.png)

Click the dropdown near the green "run" arrow and select "Add Configuration..."

![add configuration]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.58.12 AM.png)

Select "Nodemon" (or whatever you are using to run the Node server)

![add configuration]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.58.35 AM.png)

Make any adjustments needed -- in this case I need to change the value of `"program": "${workspaceFolder}/app.js",` to `"${workspaceFolder}/server.js"`

![program initial value]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.58.47 AM.png)

![change to server.js]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.58.56 AM.png)

You're now able to run your Node app with the debugger. If you haven't already, go into your application code and set a breakpoint. (If you're not sure where to start, try the first line of your route method.)

![breakpoint]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 11.59.49 AM.png)

Go back to the debugger section.

Select "nodemon" from the config dropdown.

Click the "run" arrow.

![nodemon]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 12.00.19 PM.png)


Using Postman or your browser, send a request to the endpoint where you put the breakpoint (using the appropriate request method).

![send post request]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 12.00.28 PM.png)

Visual Studio should now be in debug mode, paused on the breakpoint. You can interact with it much like you would the debugger in your browser's console. Try stepping through the code and stepping into methods.

![paused at breakpoint]({{site.baseurl}}/images/Screen Shot 2017-11-29 at 12.00.43 PM.png)
