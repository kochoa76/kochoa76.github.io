---
layout: post
title:      "Understanding Relationships with Active Record/ Rack/ HTML & CSS/ Sinatra"
date:       2018-07-29 18:26:20 -0400
permalink:  understanding_relationships_active_record_rack_html_and_css_sinatra
---


After learning Ruby, the LearnCo curriculum quickly jumped into a diverse amount of languages that carried very specific and necessary roles, each accomplishing different tasks. I wanted to compile my thoughts and teachings so far into a high level, *simple* understanding of each languages' role in the overall application, and why each is necessary. 

To begin in this blog, I'll dive into an overview of each language, and the second piece will be analyzing how each language plays a part in the overall application. 

**SQL/Active Record **

To put it simply, SQL is a language that manages data, and only data. It sole role is to speak to other databases and as a result it's often referred to as a Domain Specific Language. It is used to interact with the database that powers it, these might be MySQL, SQLlite, PostgreSQL. Why do we need data? Every time we login to a website the database takes that information and stores it so you can access your account. 

So where does ActiveRecord come in? 

ActiveRecord is the bridge between Ruby and SQL, in fact, it's a Ruby gem. If you're creating a model like I have done in my Sinatra project where a user has many gifts, and a gift belongs to a user, you will need to find a way to map this relationship within your application. If you've already created your class models for Gift and User, you need to find a way for these two models to read as tables in your application so you can add in data (i.e. username and password for the User model).  To do this you would use ActiveRecord. ActiveRecord maps your database tables to Ruby classes and database rows to Ruby instances. To set the has many and belongs to relationships you would specify in each model that a User has_many gifts and a Gift belongs_to a User via Active Record Associations in Sinatra. Easy. 

So SQL and ActiveRecord mainly work with data and mapping Ruby in an organized manner into your application. 

**Rack**

Rack is a gem that allows you to spin up a web server easily. Rack is the tool you use to get what you're creating onto the web. We will be replacing Rack with Rails soon in the curriculum (which I'm very much looking forward to! ) but it is required to use in my Sinatra Project as a way to view my application. Additionally, Rack is what Rails is built off of, and the underlying language is *Ruby*. See a pattern here? 

**HTML & CSS**

HTML is the backbone to what you're website will look like to a user. HTML will hold all of the content and some formatting but the majority of styling and formatting will be done by CSS.  This is front-end and solely caters to the client or user viewing the site. 

**Sinatra**

Sinatra is a Domain Specific Language implemented in *Ruby* that's used for writing web applications or in other words, Sinatra is a *lightweight* framework. 

What is a framework? 

> A web application framework (WAF) is a software framework that is designed to support the development of dynamic websites, web applications, web services and web resources. The framework aims to alleviate the overhead associated with common activities performed in web development.
> 

In other words, frameworks take routine and common requirements of any web application and abstract them into code so that you can spend less time creating the platform to run your application,  Frameworks allow you to focus on actually writing the code to run your application vs spending time on set up.

 Sinatra is a lightweight framework because it doesn't provide much upfront in setup. Sinatra essentially provides the bare minimum requirements to be able to run a simply Ruby based application, the rest you implement manually.
 
 **A couple key pieces before we tie everything together **
 
 MVC
 
 The reason this curriculum asks you to use Sinatra is because they want us to learn how to construct a Model View Controller (MVC) based application. MVC is a system for building web applications that governs 90% of the worlds' apps.
 
 Essentially MVC is an *understood* way to develop applications, as it delegates who is responsible for what and when. 
 
*  Model - is the underlying logic, the brains of the operation. In my Sinatra Project, the model was a Gift and a User.  Aka Ruby in the Sinatra Project. 
 
*  View - is what the client or user sees, it's purely front-end, and the only part of the MVC that the user interacts with. AKA HTML/CSS/Javascript 

* Controller - it's what communicates between the Model and the View.  It's how the logic or the brains arrives to the user/client. The controller takes each request from the User/client via the view and requests whatever necessary information from the Model.  Once the Model receives this request it sends back that necessary data to the Controller and the Controller communicates it to the View and ultimately to the User/client. In Sinatra Controllers use Ruby and routes to allow the User/client to see specific views. 

Active Record *within* Sinatra 

We learned in Active Record how to manipulate data.  In Active Record within Sinatra you learn similar methods in with CRUD (Create, Read, Update, Delete). These methods show you how your application will be able to create a user account, find or read the user account so that the user can log in once signing up to an account, update or edit their account information, and lastly how to delete their account. Sinatra provides you with the format and syntax to do this. 


**Now, we tie it all together**

So, the MVC incorporates Ruby in the Model, HTML & CSS in the view and Sinatra as the entire framework to build the application. Rack is the method in which the views are able to be seen to the User/client in the browser, and ActiveRecord is the avenue for which the developer is able to direct the Controller to write CRUD actions. 

And now, to Rails! 
 
 

