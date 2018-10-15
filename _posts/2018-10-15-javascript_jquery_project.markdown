---
layout: post
title:      "Javascript / Jquery Project"
date:       2018-10-15 20:47:04 +0000
permalink:  javascript_jquery_project
---


I found the Jquery project to be a bit awkward vs the other projects we've done mainly because it didn't feel like I was creating an entirely new project but more of an "add-on to my previous rails project. Of course, this was the purpose of this project and part of the requirements in the project guidelines but it still felt strange nonetheless.

I  have come to realize I quite enjoy Javascript. Which is pretty cool! I think it has to do with the fact that it is front-end, and with all things front end you can see your results instantly. On top of that, I have really come to learn how important user experience and styling is for the user. Particularly for me, I've realized that  just getting something to work isn't ever enough. It's making the experience useful and pleasurable for the end user that really makes a project standout. The more I dive into Javascript, the more I am realizing how important and exciting front end can be. 

As a refresh, I decided to create an app I've named UniquelyFem which is a company review app for a community of women to be able to share thoughts and experiences at work. The particular questions I've positioned include: "Are there women in leadership positions? Are there opportunities for promotion for women? Would you recommend this company to a friend?" and so on. I wanted to create a Glass Door like app but that's unique to women and issues we encounter in the workplace. 

The project requirements include: 

1. Must render at least one index page (index resource - 'list of things') via JavaScript and an Active Model Serialization JSON Backend.

2. Must render at least one show page (show resource - 'one specific thing') via JavaScript and an Active Model Serialization JSON Backend.

3. Your Rails application must dynamically render on the page at least one 'has-many' relationship through JSON using JavaScript.

4. Must use your Rails application and JavaScript to render a form for creating a resource that submits dynamically.

5. Must translate the JSON responses into JavaScript Model Objects using either ES6 class or constructor syntax. The Model Objects must have at least one method on the prototype. Formatters work really well for this.

For the index page I decided to show all the reviews created in my app to date. I decided to go against using Javascript to show all the companies created because I wanted to keep the rails layout I designed already. I hadn't yet created a view for all of the reviews so this made most sense. For the show page I decided to use js to create a "See Next Review" button for each review made within a specific company. The has many relationship was rendered via JSON within both the index and show page views I previously mentioned because each review shows that specific reviews company name so that all users can clearly know which company this review was created for. 

In creating a resource I decided to allow the user to dynamically submit a review via javascript that posts to the companies/:id/reviews route as well as renders a view of your review to the DOM via js.  Lastly, I utilized constructor syntax to create the "See next Review" piece with js. 

I battled using handlebars for the js views as it would have made sense to do so after manually creating the html/css for each js view but I decided to go against the idea towards the end of my project as it wasn't an absurd amount of styling/content. 

Feel free to check out my project here: https://github.com/kochoa76/uniquely-fem-rails-project 

Onto React/Redux! 

