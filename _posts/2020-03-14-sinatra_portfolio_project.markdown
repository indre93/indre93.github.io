---
layout: post
title:      "Sinatra Portfolio Project"
date:       2020-03-14 17:13:36 -0400
permalink:  sinatra_portfolio_project
---

For my second project with Flatiron School, I created a CRUD, MVC app using Sinatra.  Sinatra is a lightweight and flexible DSL (Domain Specific Language) in Ruby utilized for writing web applications. To put it simply, Sinatra is a bunch of pre-written code that helps us build simple and dynamic Ruby web applications.  

I decided to make a very simple and easy to use bucket list app. Where a user can sign-up, log-in and log-out. Here a user can create, edit and delete their goals, select if goal has been completed, and view not only their bucket list, but also another user’s bucket list. 

## Step 1:
The very first step I took to create this app was to use a gem called “Corneal”. This gem is a great, easy way to get the proper file structure needed to build any Sinatra app. 

To install the gem:

* Type `gem install corneal` in your terminal.
* Run `corneal new <app name>` to generate your app. 
* Run `bundle install` from your app’s directory. 
* Finally start up your server with `shotgun`. 

This is the directory structure that you will get with Corneal: 

<a href="https://imgur.com/VFEStaI.png"><img src="https://imgur.com/VFEStaI.png" title="source: imgur.com" /></a>

## Step 2:
Once the file structure is all set up and everything is running properly, we can get started with the models, which lives in the model’s folder. Model is the logic of an application, where the data is manipulated and saved. 

Since we have a database hooked up, we also need to set up migrations. The purpose of migrations is to build and structure the database (tables and columns) to help us save and manage the data associated with each of our models.  

An easy way to automatically generate both the model and migration files is by typing `corneal model <NAME>`. 

<a href="https://imgur.com/5rir820.png"><img src="https://imgur.com/5rir820.png" title="source: imgur.com" /></a>

Inside the migrate folder lives the files where we’re going to build our tables that hold our data, each attribute of the model represents the title for each column of the table:

<a href="https://imgur.com/2AfGusB.png"><img src="https://imgur.com/2AfGusB.png" title="source: imgur.com" /></a>

Below shows my model classes and their association (also some validations for when the user signs up and logs in, and as well as a method to format the date and time a goal is created to make it easier for the user to read):

<a href="https://imgur.com/zgoMHqB.png"><img src="https://imgur.com/zgoMHqB.png" title="source: imgur.com" /></a>

Once we run rake db:migrate, it’ll actually build our tables and the schema file.

## Step 3:
Now we can get started in the Controller and View part of the application. View is what the user can see, the front-end of the application. Controller is the “middleman” between the Model and the View, it communicates the data from the browser to the application and from the application back to the browser. 

<a href="https://imgur.com/ub4EQBR.png"><img src="https://imgur.com/ub4EQBR.png" title="source: imgur.com" /></a>

The main controller, Application Controller inherits from Sinatra::Base. All configurations, methods, and helper methods in this controller will be available throughout all of my other controllers. 

<a href="https://imgur.com/8kEjLjA.png"><img src="https://imgur.com/8kEjLjA.png" title="source: imgur.com" /></a>

## Step 4:
The very last step taken to finalize my project was to style my website, this is was one of my favorite steps since I was able to beautify all the hard work put into this application using CSS. 

Below is a screenshot of just the navigation part of my website (this file, “main.css” lives within the “stylesheets” folder found in the “public” folder). It is amazing how you can manipulate the way a website looks and feels! 

<a href="https://imgur.com/LwfQgXH.png"><img src="https://imgur.com/LwfQgXH.png" title="source: imgur.com" /></a>





