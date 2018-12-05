---
layout: post
title:      "React-Redux Project"
date:       2018-11-17 21:02:49 -0500
permalink:  react-redux_project
---


My final project was definitely involved. For my project I created an Ecommerce app where a user goes through the natural flow of purchasing an item online.  In addition to the act of purchasing an item I also added the ability for users to create reviews, and provide ratings of each item. The reason I chose to do an Ecommerce app lies in my desire to want to create a user intuitive front-end specific app where User Experience and design would be a priority. Up until this point I had not yet made UX and design a priority in any of my projects, and I wanted to do so this round, as I'm realizing I enjoy those two pieces in the creation process, and I thought what better way to accomplish this than with React? Although it wasn't easy it was a fun time learning how one would go about making an app for making purchases, adding to your shopping cart, and pulling product data from an API all in one.  I now understand why React and Redux were made.

There was an initial learning curve for Redux, not as much for React, but both definitely require a shift of mindset compared to the others. I think at first when learning these front-end library's you're forced to zoom in and see how each method depends on the other and get into the details about how each works individually, but once those fundamentals are solid, it's important to zoom out and ask "Why was this created this way? What problems do these tools solve?" And later, "How does react/redux fit in with my app, and what is it's purpose?".  

For Redux the key piece for me was to keep in mind that it is a tool to manage state and to leverage state in your app. That's it. This is at times hard to believe because there really is so much going on behind the scenes. 

Regarding my project, it was a challenge figuring out how to update the amount of items in a given user's cart while also increasing that specific product item's quantity. For example, if you add an a product to your cart you would expect the number in your cart to increase. However, in my scenario and specifically with the way I had setup my cartReducer when I added a product to my cart, the state of my cart would increase to one, but if I were to add a different product, the overall state would increase to two but each individual item's quantity read two, totaling four items in my cart.  As a result,  I needed to find a way to rearchitect my reducer so that I could increase my cart number if I added an item but *also* increase that specific product's item quantity. I was able to solve this issue by adding a separate hash of `item` that accepted an argument of that item's id, name, price, img_url, and description and added a counter of one when chosen to increase the cart number. In setting up my reducer this way I received that chosen product object with that item's specific id, and increased the cart number.  Using Redux's ability to update state through `mapStateToProps` simplified my process of having to pass down a product object down a few component levels.  As a result, Redux has definitely come in handy but I also now understand why it's typically best practice to try to use React to manage state as much as possible before implementing Redux as adding Redux does compound app complexity. 

 To add onto this app I would like to be able to add a product related media section to each item's page.  This would reference any videos or articles describing how to use this item, the benefits of having it, or how it adds value.   This would be a way to sell that item to a given user and add value to that user. 
 
  I feel like I could stick with these two libraries for a while, as they not only involve Javascript but I enjoyed working on  my front-end skills in conjunction with an API. I am happy for the experience of making this app and looking forward to learning more related to both these tools as I add onto this project. 



