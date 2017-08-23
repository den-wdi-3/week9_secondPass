# Week 9 Second Pass

## SEAN Stack

The SEAN Stack is not a thing.  You will probably not find documentation on it, mostly because it does not have a catchy name like "MEAN".  All we've done is subsituted Mongo for SQL, but the rest of the stack (EAN) is the same as what you used for your Rapid Prototype and Full Stack Cards app.  The only real difference is:

> We are using Sequelize to talk to SQL instead of using Mongoose to talk to Mongo.

## Project 3 Folder Structure

The backend folder structure for Project 3 will be fairly similar to your structure for Project 2.  There will be `models` and `controllers` folders on your back end, also a `routes.js` file.  

All of your front-end files will be edited in `src` and compiled to a `dist` folder. However there are a few differences of note:

- Angular is centered around a central `index.html` file that cycles out different templates using `router-outlet`, not server-side EJS or AJAX and DOM manipulation as you did in Project 2.
- You will probably need a `dbSetup.js` file to kick off your DB connection to SQL which you did not need for Project 2.  See the [Sequelize lab](https://github.com/den-materials/modeling-tunr) for a sample of how this file should look.
- You have two main options for folder organization.
  1. Separate your front and back end entirely.  Each will have its own folder, and serve up on its own port.
  2. Build the same way we did for the [Angular Universal lab](https://github.com/den-materials/angular/blob/master/lectures/day-3/angular-universal.md) or [Sequelize lab](https://github.com/den-materials/modeling-tunr), with a `server.ts` file that serves up a `dist` folder.
      - This was true in Project 2, but is worth repeating.  **Put your `server.ts` file at the same level as your `dist` folder.**  For security reasons, `server.ts` can only serve up its own folder and things below it.

## Mongo vs SQL

Selecting the right DB for the job requires a lot of thought on a development project.  There are many factors that influence this decision, including tool familiarity and comfort with different types of data organization, but in general:

- If your data is **highly related**, you want SQL.
- If your data is **plentiful, but not highly related**, you want Mongo.

These benefits often do not show themselves until very far down the road in development, so the most critical thing to do is periodically re-evaluate your data organization and needs.

[Here is a well-informed article](https://www.sitepoint.com/sql-vs-nosql-differences/) that discusses the major differences and advantages of the two database types.

## Moar SQL!

Zeb has taken [this SQL tutorial](https://sqlzoo.net/) and found it very useful.  There a couple of poorly worded problems, but for the most part it is well organized and comprehensive.

## FormControl vs FormGroup vs FormArray

- [**FormControl**](https://angular.io/api/forms/FormControl) is a mechanism for validating form input in Angular.  It wraps around an input field to make sure the data coming in through it is the type of data we want (non-empty, max-length, etc.)
- [**FormGroup**](https://angular.io/api/forms/FormGroup) and [**FormArray**](https://angular.io/api/forms/FormArray) are both ways to bundle up multiple **FormControl**s.  **FormGroup** does this as an object, **FormArray** does it as, well, an array.

Why would we choose **FormGroup** or **FormArray**?  Well, in a nutshell, do you want to pass an Object to your data storage or an Array?  If you want some more specifics, check out [this article](https://stackoverflow.com/questions/41288928/when-to-use-formgroup-vs-formarray).

You might not have seen these terms yet, because with **template-driven forms**, which we've been using in class, you get all of these features for free.  You can, however, configure your own **model-driven forms**.  [This tutorial](https://scotch.io/tutorials/using-angular-2s-model-driven-forms-with-formgroup-and-formcontrol) explains how to do this.

## Angular Is Hard!

Yup, Angular has a lot of pieces that can take a while to get your head around.  To make matters worse, with Angular 4+, you are on the cutting edge of technology, which means things are changing really quickly.  It can be really hard to find a good tutorial or course on Angular.  Here is a list of solid Angular resources.  Stay tuned for updates:

- [Team Treehouse Course](https://teamtreehouse.com/library/angular-basics-2) - a combination of videos and labs that is pretty well put together
- [Angular Tour of Heroes Tutorial](https://angular.io/tutorial)
- [Setting up an Observable](http://jasonwatmore.com/post/2016/12/01/angular-2-communicating-between-components-with-observable-subject)
- [Simple Observable Example](http://embed.plnkr.co/CJNgwR8bhKv2qY1P8rGa)
