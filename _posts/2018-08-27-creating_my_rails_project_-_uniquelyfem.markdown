---
layout: post
title:      "Creating my Rails Project - UniquelyFem"
date:       2018-08-27 22:30:17 +0000
permalink:  creating_my_rails_project_-_uniquelyfem
---


I decided to create a website that helps women gain a better understanding of a specific companies' work environment through viewing other women's reviews and experiences at that same company while in the job hunt process. I called it UniquelyFem as it addresses issues in the workplace that are unique to women. 

This project meant something to me as it is an issue I am facing today, as well as many women around me in applying for a next job. Today I am looking for a company that is supportive of women in the workplace, and ensures that women are treated fairly and equally to men. I think the job interview process can be ambiguous when it comes to sensing what kind of environment a place is, and whether they value diversity and equality.  In today's world, there really is no better way to describe a person's experience than straight from the source, and from a woman. 

If a woman's worked at a specific company, she writes a review of her experience in that company. Some of the questions, I included were: "Are there women in leadership positions within this company?", "Are there opportunities for promotion for women?", "Would you recommend this company to a female friend?", "What is your overall Job Satisfaction Rating?", salary, and other details.  These are questions I am looking to answer as I search for a company that fits my needs, so I found this project relevant and helpful--which was very exciting! 

Excitement paired with nerves, I started my project mapping out what I'd *like* my page to look like, with as many features as possible (within limits), knowing I could build from there. I set out the views, controllers (has many through relationships), and models. The tricky part was figuring out how to set up the questions I could ask such as "Are there women in leadership positions?" since I wasn't sure if that would go under the Companies or Reviews table.  Ultimately, I kept it under Reviews since I didn't have a Job table, and it worked out perfectly. I also wanted to be sure I implemented a username as an anonymous user, as this information could be sensitive to the employer. Additionally, I created a view to reference a company's details, solely monitored by the admin, including company size, location, number of employees, and an avg rating of each user's job satisfaction rating.  

I'd like to add onto this website, and make it more helpful to the user with features such as a search box to be able to filter by companies that have a rating of 4 stars or more, with women in leadership positions, located in Austin TX for example. I'd also like to add more questions relevant to the work experience such as maternity leave options, mentoring opportunities, job training, and even a way to communicate with a fellow user to ask for a referral, or ask a question you have in the interview process.

Overall, it was a scary and exciting process to create my first ruby on rails project, and I'm looking forward to adding more to it! 


