---
layout: post
title:      "Node.js + Angular.js"
date:       2018-12-30 00:23:14 +0000
permalink:  node_js_angular_js
---


As I apply to new job opportunities and read available position for junior developers I'm seeing some technologies in higher demand than others depending on the city I'm applying to. For example, in Houston TX there is a large amount of demand for .NET, PHP, Java developers and in Austin there are more Javascript technologies (React, Angular, Node) generally.  As a result of this research I've started to ask myself a few questions about what type of developer I would like to be right now. And I say right now, as I'm sure that will change the more I learn more about the industry. 

> Do I lean more to back-end or front-end development? How many front-end technologies do I know now vs back-end? Which side could I work on more to make myself more useful for employers? Which technologies catch my attention? Why? 

Throughout this process I've also spoken with a few developers and gone through the pros and cons of learning a few of the more "in demand" technologies. I have narrowed it down to two languages/frameworks I'd like to learn -- Angular and Node.js. I have used Node.js in the past but I could definitely use more experience with it, same goes for Angular. As someone who leans more to the front-end side of development, I am immediately attracted to Angular. I remember learning React and later building my first React app, and absolutely loving the experience; as a result, I feel I might equally enjoy Angular. However, I have been thinking it might be more prudent to learn Node.js, as it's a server-side language for Javascript, and as I hone my javascript skills (as I am doing now) it may make sense to pick up Node.js.  

Having been going back and forth on which technology to learn I decided to some more research on why these technologies were created and how they are used. 

**Angular.js**

 Angular is a JavaScript-based open-source front-end web application framework mainly maintained by Google to address many of the challenges encountered in developing single-page applications. It lets you use HTML as your template language and lets you extend HTML's syntax to express your application's components clearly and succinctly. AngularJS's data binding and dependency injection eliminate much of the code you would otherwise have to write. And it all happens within the browser, making it easier to work with server-side languages. 

AngularJS is what HTML would have been, had it been designed for applications. HTML is a great declarative language for static documents. It does not contain much in the way of creating applications, and as a result building web applications is an exercise in what do I have to do to trick the browser into doing what I want?

After reading up some more on Angular I began to wonder what was the difference between Angular and React as they are both under Javascript's umbrella and front-end frameworks. However, Angular is a Javascript Framework while React is a Javascript library. Angular uses a two-directional data flow process where it updates the Real DOM directly while React updates only the Virtual DOM and is concerned with the one-directional data flow. While React can be bundled with other programming libraries, Angular is a complete solution in itself. For uni-directional data flow, React needs to be augmented by Redux. 

There are a also a few versions of Angular which can increase a beginner's learning curve. Particularly, Angular 4 uses TypeScript (a more restrictive syntactically Javascript used by many companies) which adds robustness to your application. For beginners, Angular 4 is difficult to learn when compared to React since it is a complete framework but then again, React uses JSX which also took learning. 

**Node.js**

Although Node.js uses Javascript there are some distinct differences in using Node.js vs vanilla Javascript. In particular, Node.js is used as a server to interact with a database on the backend. So far while doing projects I have only used JavaScript for the front end to avoid refreshing the page while still rendering new information on the page. With Node.js you use JavaScript for the backend in order to handle requests to different urls.

One of the primary differences between Node.js and other server-side sytems is Node.js systems can serve more traffic because it has non-blocking input/output (I/O). This means it can process other tasks while waiting on the input/output operations.  For example, a Node.js server can process a request from client B while it waits for a response from a database to serve a response to client A. Most other systems will do nothing while they wait for a reply from a database to serve client A's request. Node.js also is full stack, or universal JavaScript meaning you can re-use files, libraries and modules between the server and the browser seamlessly as there are a wide range of frameworks and tools for browser Javascript.

The downsides in using Node.js involve its ability to handle a large amount of traffic; for example, implementing many algorithms would require the client to wait until that computation is finished before moving forward. Another issue with Node.js is the use of NPM or node packaging manager and it's constantly changing updates. There are many packages and modules created and updated so it is more difficult to maintain consistency with Node.js vs other server-side languages. I actually heard this frequently when speaking with other Node.js developers, there are constantly new updates to keep track of with Node.js, and less conventions. 

I've started working on a new project to learn other technologies and frameworks to build a full stack web app. For this project I am utilizing Node.js, MongoDB, Express, and React to build an app that sends a user an email with a request to log into a web app (one I've built) and fill out a survey created by the admin user.  The app is designed for an end user looking to gain insight from their customer install base. I will be discussing it later in my blog but so far it's been interesting to see new code in action. 

In conclusion, I think it depends on what roles and types of companies I'm looking for. It looks like startups are more interested in hiring Javascript friendly developers while larger corporations look for Python, Java, and .NET developers.  In addition, if I am trying to lean into more front-end technologies, I would like want to consider Angular. I think overall, it would make sense for me to learn both as a beginner developer looking to learn up-and-coming technologies.

