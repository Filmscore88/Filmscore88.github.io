---
layout: post
title:      "Sinatra Portfolio Project"
date:       2019-05-13 13:13:03 +0000
permalink:  sinatra_portfolio_project
---


It is pretty amazing to see how much work goes into building a dynamic web app. At least with Sinatra. Even though this may be the case, i definately enjoyed the whole process. 

Im going to cover 3 main points about the project,  RESTful routes , forms,  and password security.  

   If you ever  work on a team project, or pick up on someone elses unfinished project the use of conventions will facilitate the abilty for you to understand what exactly is going on . With HTTP requests, when a user clicks on a link, we want to make sure we understand what our routes are doing. After completing the project I have come to see the importance of this. At first it took me some time to grasp the flow of CRUD activity (Create, Read, Update, Delete), but once it made sense to me it was pretty simple to see what the next step was. You have to put yourself in the users position, and ask yourself questions they might ask themselves. 
	 
	 We now come to my experience with forms.  I would say it is very important to get a solid understanding of CRUD along with RESTful before writting forms that will "delete" or "post" and user data. This is a tremendous responsability. If you imagine that there are a million users using your application, and they are putting personal data into these forms and submitting them to you. Therefore, it is important to not only make sure the users data does not get lost, but also make sure it is secure. Which brings me to my last point. 
	 
	 Working with password security features such as "password digest"  was awesome. In fact I remember watching a video  that discussed how such features work. In this example of "password digest",  it comes with the gem called "bcrypt" that basically creates a particular key that is seperate from the password. So in the case of a hacker getting access to that users password, they also need access to the randomly generated encryption key which is  a long set of numbers produced by your gem not the user.
	 
	This was so far the most fun I have had working on a project, and seeing what goes on under the hood from the minute send a HTTP request to a website, to the minute I login to my account was incredible. 


