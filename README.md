# Week 9 Second Pass

## SEAN Stack

The SEAN Stack is not a thing.  You will probably not find documentation on it, mostly because it does not have a catchy name like "MEAN".  All we've done is subsituted Mongo for SQL, but the rest of the stack (EAN) is the same as what you used for your Rapid Prototype and Full Stack Cards app.  The only real difference is:

> We are using Sequelize to talk to SQL instead of using Mongoose to talk to Mongo.

## Project 3 Folder Structure

The folder structure for Project 3 will be almost identical to your structure for Project 2.  There will be `models` and `controllers` folders on your back end, also a `routes.js` file.  All of your front-end files should be served up in a `public` file.  However there are a few differences of note:

- Angular is centered around a central `index.html` file that cycles out different templates using `ng-view` and `ngRoute` or something similar.  
  - Put this `index.html` inside your `public` folder so all you have to do is serve up the `public` folder, and the browser will load it by default.
  - Since these templates are being generated with Angular on the front end, it is a good idea to put these templates inside a `templates` folder inside `public`, as opposed to putting them in the same folder as `server.js` on the back end as we did for project 2.
- You will probably need a `dbSetup.js` file to kick off your DB connection to SQL which you did not need for Project 2.  See the [Sequelize lab](https://github.com/den-materials/modeling-tunr) for a sample of how this file should look.
- This was true in Project 2, but is worth repeating.  **Put your `public` folder in the same folder as `server.js`.**  For security reasons, `server.js` can only serve up its own folder and things below it.

## Mongo vs SQL

Selecting the right DB for the job requires a lot of thought on a development project.  There are many factors that influence this decision, including tool familiarity and comfort with different types of data organization, but in general:

- If your data is **highly related**, you want SQL.
- If your data is **plentiful, but not highly related**, you want Mongo.

These benefits often do not show themselves until very far down the road in development, so the most critical thing to do is periodically re-evaluate your data organization and needs.

[Here is a well-informed article](https://www.sitepoint.com/sql-vs-nosql-differences/) that discusses the major differences and advantages of the two database types.

## Moar SQL!

Zeb has taken [this SQL tutorial](https://sqlzoo.net/) and found it very useful.  There a couple of poorly worded problems, but for the most part it is well organized and comprehensive.
