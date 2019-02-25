---
layout: post
title:      "GlowEcommerce Add Ons "
date:       2019-02-03 22:28:28 -0500
permalink:  glowecommerce_add_ons
---


I've been meaning to build on my Ruby/Rails and React/Redux project GlowEcommerce for some time, and wanted to dedicate this blog to scope the impending features and add ons.  

GlowEcommerce, is an Ecommerce App providing a place to easily purchase beauty products. I placed a focus on building out the UI for the app so the actual ability to purchase an item through a payment system has not been implemented.  I'd like to focus the next two pieces of my projects to adding these two features: a payment system, and an immediate email to the person who's recently made that purchase with a receipt. Following these two pieces, I'd like to persist the cart (items a user has added to their cart) to the server, so that even if you refresh the page, you will still have your given state included with your cart. 

All in all there are 3 pieces I'd like to add: 

1. a payment system 
2. receipt to purchaser 
3. persisting cart state to server 

**Payment Sytem**

At the moment I'm building a MongoDB-Express-React/Redux-Node.js app that's called EFeedback providing  feedback-collection for any business looking for feedback from its users. This app provides everything from authentication to email handling.  The app sends mass emails to a big list of users for the purpose of collecting feedback. The app also includes a payment system to purchase this service using Stripe.

I'm about 2/3's of the way through fully building this app but I've been building it using Stephen Grider's Udemy course 'Node & React Full Stack App'.  It's been very thorough and helpful to have someone explain the concepts of building a full stack app with a different architecture design than GlowEcommerce. Additionally, I implemented Google oauth authentication for the signin process which I hadn't done with GlowEcommerce (considering implementing it -- I'll add it to the list :0 ).

Stripe is the system used within this course and as a result I will be implementing Stripe as the payment system for GlowEcommerce. There are a few benefits and drawbacks I've learned from my Stripe research, defined below: 

Benefits: 
*    great documentation 
* 	 Excellent developer tools
*    Predictable flat-rate pricing
*    Advanced reporting tools
*    Ideal for international merchants
*    Excellent marketplace tools
*    Excellent subscription tools
*    Multi-currency support
	 
Drawbacks: 
*   Account stability issues
*   Not suitable for high-risk industries
	

**Receipt to Purchaser**
	
To add onto the benefits of Stripe, the system includes the ability to send an email with a receipt of the user's purchase as well as a receipt of any refund to the user.    
	
I've yet to build this piece of the app (Stripe) with Efeedback, but I"m looking forward to it. 
	
**Persisting Cart State to Server**
	
In terms of persisting state to the server, I could create an action method within Redux that 'posts' the item selected to add to the cart to the backend through a fetch request which updates the database with the cart item quantity.  This would involve some redesign but nothing that hasn't already been implemented in the app already. 
	
I plan on finishing Efeedback prior to starting to add these changes to GlowEcommerce. I'm looking forward to making more progress and learning more about building Ecommerce specific applications. 
	
	
	
	
