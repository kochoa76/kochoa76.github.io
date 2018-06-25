---
layout: post
title:      "Breaking down my CLI Project "
date:       2018-06-25 17:17:11 -0400
permalink:  breaking_down_my_cli_project
---


Today I finished my CLI project. It was quite a week, working an average of 8 hours a day, but overall I'm happy with my result, and with myself. 

The project asks you to create a CLI that accesses data from a webpage.  I decided to build my project around Goodreads' website, a "social cataloging" website that allows individuals to freely search its database of books, annotations, and reviews, it also allows users to generate library catalogs and reading lists. 

I went with Goodreads because I personally enjoy reading, it's a great way to jump into someone else's world and live a different life, if only for a while. And to me, reading an entire book is so much more difficult and rewarding than watching a show or movie. I always feel a tiny sense of accomplishment when finishing a book. As a result, I decided if I was going to read a book, I wanted to ensure I read a *great* book, one that adds a little something to my life, whether it be perspective, motivation, or humor. That's when I started referencing Goodreads. Before reading any new book, I usually check and see if they have anything close to a 4 star rating or above. 

Brainstorming off of this, I decided to pull a list of books off Goodreads specifically a list they provide weekly "Popular Books this week." I liked how this list provided only 50 books that updated weekly according to the book's ratings,  as well as how many people were "currently reading" each book. These parameters ensure you'll find a great book as well as a relatively newly published book. Here is the Goodreads' list for reference: https://www.goodreads.com/book/most_read

The toughest part of the project for me lies in how to architect the layout and in deciding how each object collaborates with one another. I personally went back and reviewed the previous CLI labs as well as referenced a good amount of Avi's old videos to help with the design of the project layout. When it came to scraping the page and pulling the data from the website I found that the process was easier than expected. It took time but eventually I was able to find what I was looking for, and extract the data as I planned to. 

I'd say the more challenging piece of the project was going the next layer deep and extracting data from each individual book's website, which involved having to click that book's page and scrape that data (book's synopsis). Figuring out how to use the CLI's input to pull up a book's name outside of the class's scope, while simultaneously calling a method to scrape the book page's website and print out the book's synopsis was my greatest challenge, and I was very excited to finally get it to work. 

Overall it was really exciting to be able to create something on my own from scratch and see it work the way I designed it to.  I'm very much looking forward to more projects soon. If you'd like to see my CLI project you can view it here: https://github.com/kochoa76/Most-read-books-cli-app or you can find it published on Ruby Gems here: https://rubygems.org/gems/most_read_books





