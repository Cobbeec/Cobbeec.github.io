---
layout: post
title:      "My Rails Project"
date:       2021-02-14 17:08:51 +0000
permalink:  my_rails_project
---


When I first started my Rails project, I was thinking primarily about my models and setting up my ActiveRecord associations correctly. I knew this was the foundation of my project. I was initially trying to set up an app that connected users to books, and then users would have many books and have many authors. The tricky part came when realizing that there might be multiple and duplicate books and authors entered in the database. Instead my cohort lead suggested that I use reviews to belong to my users. These would be unique to the user, and the book and author objects would exist independently. This set up both made sense and fulfilled the project requirements. I had a model that had two belongs_to relationships, and I had several candidates for my nested routes, as I had a few parent and child relationships. If I were to go and build my project out more, I would like to add the ability to comment on reviews, and allow the community of users to better organize both their and others’ reviews. I would also like to have added an aliased route to challenge myself. 

Another key lesson I learned was about the perils of bad data. I made this project in a bit of a piecemeal order, and I started instantiating and saving objects before I added my validations. I also created and saved users before I added my Omniauth. One of the learn.co lessons says of bad data that “is the bogeyman of web applications: it hides in your database until the worst possible moment, then jumps out and ruins everything by causing confusing errors.” This is absolutely true. At one point I could only get my logout method to work for Omniauth users but not users who signed up on the app. I repeatedly checked my code, and couldn’t find any errors. I realized the issue was with my older users created before I had any kind of validations. I reset my database and tried again. I also ended up with duplicate and blank objects that caused strange errors. I now have a brand new appreciation for validations. They are so easy to use and save a developer many headaches. I also have a new appreciation for the command “rails db:reset.” I had to completely clear out my database a few times, but it ultimately made the process much easier. 

Overall this project was very challenging. It brought together so many old skills and so much new knowledge: setting up models, CRUD functionality, authentification, DRYing up code, using partials, protecting routes, and the pain that is nesting routes. I did enjoy it though, and I hope my finished product speaks to that. 

