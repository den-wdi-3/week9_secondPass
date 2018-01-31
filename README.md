# Week 9 Second Pass

## SEAN Stack

The SEAN Stack is not a thing.  You will probably not find documentation on it, mostly because it does not have a catchy name like "MEAN".  All we've done is subsituted Mongo for SQL, but the rest of the stack (EAN) is the same as what you used for your Rapid Prototype and Full Stack Cards app.  The only real difference is:

> We are using Sequelize to talk to SQL instead of using Mongoose to talk to Mongo.

## Project 3 Folder Structure

The backend folder structure for Project 3 will be fairly similar to your structure for Project 2.  There will be `models` and `controllers` folders on your back end, also a `routes.js` file.  

All of your front-end files will be edited in `src` and compiled to a `dist` folder. However there are a few differences of note:

- Angular is centered around a central `index.html` file that cycles out different templates using `router-outlet`, not server-side EJS or AJAX and DOM manipulation as you did in Project 2.
- You will probably need a `dbSetup.js` file to kick off your DB connection to SQL which you did not need for Project 2.  See the [Sequelize lab](https://github.com/den-materials/modeling-tunr) for a sample of how this file should look.
- For folder organization locally, separate your front and back end entirely.  Each will have its own folder, and serve up on its own port.
  - This was true in Project 2, but is worth repeating.  **Put your `server.js` file at the same level as your `dist` folder.**  For security reasons, `server.js` can only serve up its own folder and things below it.

## Mongo vs SQL

Selecting the right DB for the job requires a lot of thought on a development project.  There are many factors that influence this decision, including tool familiarity and comfort with different types of data organization, but in general:

- If your data is **highly related**, you want SQL.
- If your data is **plentiful, but not highly related**, you want Mongo.

These benefits often do not show themselves until very far down the road in development, so the most critical thing to do is periodically re-evaluate your data organization and needs.

[Here is a well-informed article](https://www.sitepoint.com/sql-vs-nosql-differences/) that discusses the major differences and advantages of the two database types.

## Moar SQL!

Zeb has taken [this SQL tutorial](https://sqlzoo.net/) and found it very useful.  There a couple of poorly worded problems, but for the most part it is well organized and comprehensive.

## NgModule

From the Angular guide:

> An NgModule is a class marked by the @NgModule **decorator**. @NgModule takes a metadata object that describes how to compile a component's template and how to create an injector at runtime. It identifies the module's own components, directives, and pipes, **making some of them public**, through the exports property, **so that external components can use them**. @NgModule can also add service providers to the application dependency injectors.

If you would like more information, check out [this section of the Angular guide](https://angular.io/guide/ngmodules).

## Angular Is Hard!

Yup, Angular has a lot of pieces that can take a while to get your head around.  To make matters worse, with Angular 5+, you are on the cutting edge of technology, which means things are changing really quickly.  It can be really hard to find a good tutorial or course on Angular.  Here is a list of solid Angular resources.  Stay tuned for updates:

- [Team Treehouse Course](https://teamtreehouse.com/library/angular-basics-2) - a combination of videos and labs that is pretty well put together
- [Angular Tour of Heroes Tutorial](https://angular.io/tutorial)
- [Setting up an Observable](http://jasonwatmore.com/post/2016/12/01/angular-2-communicating-between-components-with-observable-subject)
- [Simple Observable Example](http://embed.plnkr.co/CJNgwR8bhKv2qY1P8rGa)
