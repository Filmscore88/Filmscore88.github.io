---
layout: post
title:      "React/Redux project"
date:       2019-08-19 14:27:11 +0000
permalink:  react_redux_project
---


The idea behind React is amazing. If you think about how HTML and JS is written normally, with an index page and a page for every class you would be using in your JS files, that ends up looking like a lot of code and not only that, a lot of that code gets reused throughout your application. That is where Redux  comes in with the concept of ```components```, which basically take a chunk of code and place it in a container and have the ability to reuse it and not only that but also pass down ```props``` and ```state```to that component. 

This might sound confusing but this demonstratoin may help. 

Lets say you have a button tag: ```<button type= "radio" />  ``` the type of the button changes what that buttons property is. In the same way when we create our own components, say <Cats type={black}/>   the cat is our component,  and the type is  our ```props``` being passed down to that Component.  So what that allows us to do is pass down properties to our components that are able to be used by them but not manipulated.  If we were to want to manipulate our properties, we would need to be introduced to the concept of ```State```.  State is basically an object with properties.  These properties can be changed only if the component is a class component: 
``` class Cat React.Component {
           constructor(){
					 super()
					 
					 this.state= {
					  color: "brown" 
						}
				}
				
				return() {
         render(
						<div> 
							 {this.state.color}
							 </div> 
						 )
				}		 ```
				
				In this basic example we see the structure of a class component in order to be able to use state and manipulate it. 
				
				Although there is much more to React and using components and state, I this explanation helped to understand the concept of props and state a little bit more. 
				
				
				
