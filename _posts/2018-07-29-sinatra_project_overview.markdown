---
layout: post
title:      "Sinatra Project Overview "
date:       2018-07-30 01:14:18 +0000
permalink:  sinatra_project_overview
---


For our Sinatra Project we were instructed to create a an MVC Sinatra application using Ruby,  ActiveRecord with Sinatra, Sinatra, Rack, and HTML/CSS. The application would comprise of multiple models with a has many / belongs to relationship,  and the abilty to create, read, update and destroy any instance of the resource that belongs to a user. If a user creates an instance, they should be the only user to edit or delete it. Lastly, they required validations for user input. 

I decided to create my app based on a Gift Journal. A Gift Journal is similar to keeping a journal, but is specific to gifts or items you may desire but aren't willing to splurge on for yourself just yet. Gift Journal allows you to keep track of your desired gifts for your records or even for others as brainstorming for gift giving. 

The model allowed for a clean associations, a gift belongs to a user, and a user has many gifts. In addition to allowing for CRUD actions for each model, the application would also provide a view of other users who have created accounts, as well as a view of all the gifts registered in the application. 

I think moving forward I would like to build on the functionality and allow for a given user to be able to share their gift journal with other users--such as family and friends-- who may want to take a peek at their journal for upcoming birthdays, Christmases, and events.

The project idea stemmed from a desire for something similar. My family has very little spontaneity when it comes to gift giving. We ask what the other wants and we deliver. In many ways knowing what you're getting is nice in that you're getting something you want, but on the other hand it doesn't leave room for excitement or adding thought and consideration to a gift.  I thought Gift Journal met in the middle. With Gift Journal, you can get a feel for the types of gifts a person may like, and also add in spontaneity and fun to gift giving! 

In terms of working through the project, I found the most difficult part of working on this project was getting my app live on Heroku, while also simulatenously running it in git. For some reason many of the students in my cohort, including me,  were having problems after running the app on Heroku. After exiting from the git repo and cloning down the repo into git to add to the app, shotgun would no longer work, and instead try to connect to my localhost--this happened to me 3 times. As a result, I had to create an entirely new repo in github copy/paste in all my previous code and deploy it on heroku. It was a bit of a nightmare. I would recommend anyone who encounters this issue to not deploy on Heroku until the very last step of your project. 

Ultimately, it was a great learning experience. I feel like I did get a solid understanding of how these languages work together, check out my blog written about this topic, <a href="[http://kaylaochoa.com/understanding_relationships_active_record_rack_html_and_css_sinatra]"> here </a>. Ultimately, I'm looking forward to seeing how Rails' magic works! 
