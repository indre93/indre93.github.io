---
layout: post
title:      "CLI Data Gem Project # "
date:       2019-07-19 00:43:45 +0000
permalink:  cli_data_gem_project
---

Hi! my name is Indre and I am studying to be a Software Engineer at Flatiron School. Below, I will be discussing about my first project ever created when it comes to coding, and I will also be describing the process on how this was done.

Creating my first project was quite intimidating, especially with the fact that a little over 6 months ago computer programming was completely foreign to me. So this project definitely put into test everything I have learned so far and it also made me realize how much I actually enjoy coding.

So, since I also love working out and it is such an essential thing to do for our own well-being, I decided to build a CLI application about exercising. This application provides the user with a list of exercises based on the body part selected. I also decided to go an extra “level deeper” by letting the user select the desired exercise and included instructions, and as well as a video to show the proper way to perform the exercise.

Now, let’s get into the fun part and talk about the steps on how I built my CLI application:

### **Step 1: Creating directory** ###

First, I needed to create a directory with the proper structure, and the basic requirements needed to create my new gem. To do so, I simply typed the following command:

<a href="https://imgur.com/MM9Y1tM"><img src="https://i.imgur.com/MM9Y1tM.png" title="source: imgur.com" /></a>

Typing the `bundle gem <project-name>` command will generate a project skeleton.

### **Step 2: Adding executable file** ###

Then I added the following code in the *bin/project-name* file:

<a href="https://imgur.com/fvX4LJ8"><img src="https://i.imgur.com/fvX4LJ8m.png?1" title="source: imgur.com" /></a>

The code in line 1 is known as “shebang”. This line lets the shell know which interpreter to use to run the application.

The code in line 2 will load the *environment.rb* file, which holds the required gems and files to execute the application.

The code in line 5 starts the application using the *#start* method, which is defined in the *Cli.rb* file within the *lib/* directory.

### **Step 3: Making file executable** ###

Next, I needed to make the *bin/project-name* file executable by giving it permission. To do so, I used the `chmod +x <project-name>` command as follows: 

* `cd bin/` to go into the bin directory 
* `ls –lah` to check permissions 
* `chmod +x <project-name>` to give it permission

Now we can simply type `./bin/<project-name>` to execute the application!

### **Step 4: Defining classes, methods, and modules** ###

All the information about the exercises was obtained by scraping it out of a website using *Nokogiri*. I scraped the data from the HTML document that makes up the web page used and put this code in the *Scraper.rb* file.

<a href="https://imgur.com/nrY4NTv"><img src="https://i.imgur.com/nrY4NTvl.png" title="source: imgur.com" /></a>

In the *concerns* directory, I created a *memorable.rb* file. Here I put the module that holds the class and instance methods that are used by the other classes to avoid repetition.

The methods defined in this module are accessed by the other classes by using the *include* keyword for the instance methods and the *extend* keyword for the class method.

<a href="https://imgur.com/177VKgO"><img src="https://i.imgur.com/177VKgOm.png" title="source: imgur.com" /></a>

The code the user will be interacting with lives in the *Cli.rb* file.

<a href="https://imgur.com/3Ym96Uv"><img src="https://i.imgur.com/3Ym96Uvl.png" title="source: imgur.com" /></a>

Once the application is executed by the user, this file brings together all the code scraped and written in the other files, within the *lib/* directory, to make this application work.

<a href="https://imgur.com/yiluIZY"><img src="https://i.imgur.com/yiluIZYl.png" title="source: imgur.com" /></a>

To make my application a bit more appealing and user-friendly, I added some color by using the *colorize* Ruby gem.
