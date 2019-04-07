---
layout: post
title:      "Diving into the Developer World "
date:       2019-04-07 22:51:41 +0000
permalink:  diving_into_the_developer_world
---

# Building a gem from scratch 

![](https://www.globalhealingcenter.com/http://)


Choosing Global Healing Center's supplement line as my first Ruby CLI gem was an easy decision. Im a big advocate for health, and personally have taken most of their supplements.  For our CLI project, we were required to scrape data from a website and choosing an easy website to scrape was ideal. Im sure I could have found an easier website to pull data from, however I was determined to stick with that website even if it meant extra work to finish my project. 

  When tackling any software development project, it is important to look at the big picture and ask yourself  **WHAT?** am I working on. For my project, I was to essentially build a Command Line Interface gem that would interact with the user and display data of which I was to scrape.  A ruby gem is basically a package manager for the Ruby language that helps in providing a format for the distributing Ruby programs and libraries. Part of the beauty of programming is that anyone can contribute to the language to some degree. A language such as Ruby comes with basic methods and objects, but developers contribute to the basic by providing tools such as gems through which programmers can do even more with their code. For example, for my CLI gem project I wanted to add color to my CLI output. Therefore, I utilized a gem called colorize. 
	
	 Once you have Ruby installed, you can use a gem by first installing one in this manner: 
	 `command gem install <GEM_NAME>.` 
	 
However, before getting to the point of adding gems such as colorize to make my project look "pretty" I had to write my program. So I asked myself these questions:
	 
1. 	 What data would the user of my program need?
2. 	 How much data am I going to scrape?
3. 	 Is the data I am scraping accessible on a single webpage?

1- If I were to browse a supplement website, I would definately want to know more about what a particular supplement is. Some supplements such as Vitamin C are pretty descriptive as to what they are, however, with the Global Healing Center supplement line it is not the case. 

2- I decided a brief description of the product and a url link to the product would be sufficient.

3- Sometimes getting additional data from a webpage requires opening another link to access that date, fortunately for me I could access it all from a single page! 


 I began by creating bundle ruby gem for my project by running` bundle gem global_healing `  in my terminal (bash). I really loved what this did for me as it provided preformatted files and directories where all my code will live in.

```
- bin
- lib
.gitignore
travel-inspiration.gemspec
Gemfile
License.txt
Rakefile
README.md
```

This really took off the "bundle" of nerves (pun) I had in starting my project. In the lib directory, there is a sub directory called global_healing that was home to all of the files I created. In order to demonstrate competency of everything I had learned thus far, I had to keep the Single Responsibility Principle in mind. This means that for every object I create, I had to make sure that it was responsible for 1 purpose. 
    Therefore, I created 3 files in this global_healing directory each responsible for 1 thing. My cli.rb file was responsible for the CLI portion of my program, when I was to run my program , all the logic responsible for instantiating new objects and displaying all my data to the user interface would live here. 

   Next was  the scrapper.rb file, which would be responsilbe for scrapping the neccesarry data of the web using gems such as Nokogiri and Openuri to do so. These gems are a real beauty, I would imagine if there were no such thing, writting a program to achieve such results would be quite a task for a newbie such as myself. So I want to give a shout out to the minds behind those gems and a thank you for their hard work. Finally, I created a supplements.rb file which was responsible for colaborating with the scrapper class and taking the data scraped and instantiating new instances of supplement objects with attributes pulled from the web by the scrapper class. 
	 Once all these files were properly programmed it was time to see all the magic happen and run the program by calling a new instance: `GlobalHealing::CLI.new.call` of my CLI class in the bin directory global_healing file. 
	
	You can view my project Github repo link here!
	https://github.com/Filmscore88/global_healing






