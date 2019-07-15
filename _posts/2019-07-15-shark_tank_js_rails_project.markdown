---
layout: post
title:      "'Shark Tank' Js/Rails project"
date:       2019-07-15 05:56:33 +0000
permalink:  shark_tank_js_rails_project
---


When creating dynamic web application,  it seems very effecient to use of ajax with javascript to render content to your view pages.  For this project, I  found it very helpful to look at other sample projects and to get an idea of how to organize my code in different files, so I will go over some important steps that will help anyone working on this project. 

First, you want to add gems that will be required in order to be able to use javascript in your gem file:

```  gem 'jquery-rails'
      gem 'active_model_serializers', '~> 0.10.9'   ```


In order to have access to json objects (javascript object notation objects) in your javascript files, you want to create what is known as a *active model seriealizer*.  How this works im not quite sure yet, however it will be important to have these files in order to move ahead.  You will have to generate these models according to the specs of your current rails app models and include any has_many, belongs_to , as well as attributes for your model: ```attributes :id, :name, :description, :user_id```.  Finally in order to generate the models you will have to run ```rails g serializer <model name>``` in your terminal which will create a file with set up serializer model structures with some default specs that can be modified according to your model structure. This only covers the bare minimum, however hopefully it can help you be if even 1 step ahead and on the right track. 
