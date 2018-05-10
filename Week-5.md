# Week 5 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

### 1. What are some advantages of using Ruby on Rails?
One advantage of using Ruby on Rails is that you can test your code using Capybara.

Google:
It requires less coding, increased development speed, ease of maintenance, large community for assistance, constantly improving technology.

### 2. How does Ruby on Rails use the Model View Controller (MVC) framework?
In Ruby on Rails, MVC is used as the framework for it's applications. It separates it into the following components and does the following:
Models - handles data and business logic
Controllers - handles the user interface and application
Views - handles graphical user interface objects and presentations
This separation results in user requests being processed as follows:
1) The browser from the client sends a request for a page to the controller on the server
2) The controller retrieves the data it needs from the model in order to respond to the request
3) The controller gives the retrieved data to the view
4) The view is rendered and sent back to the client for the browser to display

A controller's purpose is to receive specific requests for the application. Routing decides which controller receives which requests. Often, there is more than one route to each controller, and different routes can be served by different actions. Each action's purpose is to collect information to provide it to a view.
A view's purpose is to display this information in a human readable format. An important distinction to make is that it is the controller, not the view, where information is collected. The view should just display that information.

### 3. Using the information given, complete the steps for creating a new view in a rails app by filling in the blanks:

  1. Create a route:

  code:
  ```
  get '/about' => 'statics#about'
  ```
  file: config/routes

  2. Create the ____________

  code:
  ```
  class ____________ < ApplicationController

  def about
    _______________________
  end
  ```

  file: _____________________

  3. Create the View

  code:

  ```
  <div>This is the About page!</div>
  ```

  file: _____________________


### 4. Look at these sets of Rails routes, they are an example of which principle/term that we touched on briefly in class? Find the term, and explain why it is important.

```
/users/       method="GET"     # :controller => 'users', :action => 'index'
/users/1      method="GET"     # :controller => 'users', :action => 'show'
/users/new    method="GET"     # :controller => 'users', :action => 'new'
/users/       method="POST"    # :controller => 'users', :action => 'create'
/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
/users/1      method="PUT"     # :controller => 'users', :action => 'update'
/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
```

### 5. What is the public folder used for in Rails?

The public folder is used to have those views that would be publicly accessible in the application.

### 6. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

get '/game' => 'main#guess'

### 7. What are cookies for? How do they work? What is the difference between a session and a cookie?

Cookies are small files containing data specific to a particular client and website that are stored on a user's computer.

A session only lasts for the duration of users using the website while cookies are stored in the computer and can later be retrieved.

### 8. In an html form, what does the "action" attribute tell you about the form?  How do you designate the HTTP verb for the form?

The "action" attribute tells the browser what page to call once it's submitted.
You designate the HTTP verb by specifying the method, ie 'get' or 'post'.

### 9. Why would you use an instance variable in a rails controller?

You would use an instance variable in a rails controller to send it to the appropriate view file so they can render it on the browser.

### 10. Name two rails generator commands and what files they create:

rails generate controller “file name” “first method”
-creates controller and method

rails generate model Article title:string text:text
-creates new model, title attribute of type string, and text attribute of type text

### 11. Rails has a great community and lots of free tutorials to help you learn. Here is a list of some tutorials to choose from, choose one, do it, and then report back here at least one thing you learned. You can also use a different resource if you find one that you like better.

- https://www.tutorialspoint.com/ruby-on-rails/index.htm
- http://railsforzombies.org
- http://guides.rubyonrails.org/getting_started.html

Migrations are Ruby classes that are designed to make it simple to create and modify database tables. Rails uses rake commands to run migrations, and it's possible to undo a migration after it's been applied to your database. Migration filenames include a timestamp to ensure that they're processed in the order that they were created.
