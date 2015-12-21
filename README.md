# Scott Thompson
# 537_final_project
# Project README

For my final project I created a web-based blog application using the Ruby on Rails framework. As you know, I learned a great deal of the Ruby programming language for my work on Project 2, so this was a natural final project to me. I've also gained a lot of interest in doing more work using Ruby on Rails in the future. 


Before I explain the features and app structure you need to make sure you have Ruby *and* Rails installed. Below are some links to help you get started:

Windows http://rubyinstaller.org<br>
OS X/Linux http://rubyonrails.org/download/<br>

Rails is a framework written in the Ruby language. It too follows the motto of 'Convention over Configuration' by not requiring app interactions to be coded one way, but you gain tremendous benefits by following community established guidelines. Rails generates nearly all the basic file structure for the entire app right away. This allows more time to focus on writing the strongest Ruby code you can in your Models, Views, and Controllers. As you might imagine Rails follows the MVC structure. To demonstrate the power of the Ruby on Rails framework as well as show off my personal knowledge of Ruby, I created a BuzzFeed-style blog app called 'HawkFeed' which is for MSU students who love their school. I will list out the many areas where I contributed code in this structure below based on category.

Models

HawkFeed has two models: Article and Comment

These models affect how data is saved in the application. It also establishes the relations that serve as the database schema. You can see the model code in these two files:

  app/models/article.rb
  app/models/comment.rb

Views

There are multiple views I created for the user to interact with the application. If you follow certain naming conventions in Ruby on Rails, your views interact tightly with your controllers. So there are views for articles, comments, and the landing page. Articles have index, show, new, and edit views which perform the exact functions you think they would. There also is a partial view for forms. Partials in Rails come from the other Ruby mantra 'Don't Repeat Yourself'. You create a 'DRY' piece of code that can be rendered in other views. The views for comments are both partials that are rendered in the articles views. Views for Ruby on Rails are in the '.html.erb' format which stands for 'embedded Ruby'. Embedded Ruby files dynamically generate HTML that the user sees. Navigate here to see the view files:

  Articles
    app/views/articles/index.html.erb
    app/views/articles/show.html.erb
    app/views/articles/new.html.erb
    app/views/articles/edit.html.erb
    app/views/articles/_form.html.erb
    
  Comments
    app/views/comments/_comment.html.erb
    app/views/comments/_form.html.erb
  
  Welcome
    app/views/welcome/index.html.erb

Controllers

I created three controllers to imbue my HawkFeed application with logic and features. I created an Articles controller with CRUD (create, read, update, destroy) capabilities that also uses strong parameters for increased reliability. I also created a Comments controller with create and destroy capabilities that also uses strong parameters. Last I created a basic Welcome controller with read capability. The controller files can be found below:

  app/controllers/articles_controller.rb
  app/controllers/comments_controller.rb
  app/controllers/welcome_controller.rb

Database

Ruby on Rails makes database creation and management a complete breeze by generating schemas and migrations automatically if your code is following established conventions. Just one look in either of the controllers and you can see how easy it is to create complex and powerful queries to your database using Ruby's built-in method chaining. See the files here:

  db/development.sqlite3
  db/schema.rb
  db/migrate/20151220225036_create_articles.rb
  db/migrate/20151220235028_create_comments.rb

Authentication

My website also uses Ruby on Rails' built-in basic HTTP authentication for creating, updating, and destroying articles as well as deleting comments. The following credentials work for my app:

  username: admin
  password: 12345
  
Boostrap

I also did some basic bootstrap CSS and SASS (a CSS variant that works well with Ruby on Rails) to do simple cleanup of the site while helping it work better across different browsers. If there is one thing I wish I knew how to do better at the end of this class is front-end web development. I hope looks don't matter *too* much.

Running HawkFeed

To run HawkFeed, simply make sure you have Ruby *and* Rails installed (See above for instructions). If you feel like it you can pull from this repository. Then, in Terminal, navigate to the root app directory scott_thompson_final_project and run the command:

  bin/rails server
  
This starts up the built-in web server for Ruby on Rails (How cool is that?!). Now navigate your browser to localhost:3000/ and enjoy the app!

I encourage you to look through the commit history of this repository to see how I built this application. 

I also hope to eventually make this web app live through the Heroku platform, and I will update this README when I do.
