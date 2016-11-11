# Rails as an API Study

Use your favorite search engine and the provided readings to research and answer
the following questions (no prior knowledge is expected).

In your answers, be sure to cite any relevant sources you consulted in your
search. We ask you to write answers in your own words in order to see how you
process what you've read. Please do not answer with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [rails-api-template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   [Starting Ruby on Rails: What I Wish I Knew | BetterExplained](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
-   [Intermediate Rails: Understanding Models, Views and Controllers | BetterExplained](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)
-   [The Rails Command Line — Ruby on Rails Guides](http://guides.rubyonrails.org/command_line.html)
-   [Rails Routing from the Outside In — Ruby on Rails Guides](http://guides.rubyonrails.org/routing.html)
-   [Action Controller Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/action_controller_overview.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
The responsiblity of the model layer is to talk to the database and perform the
business logic.  It takes in a request from the controller and then passes the
resource being requested back to it.

Resources:
https://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/
https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The responsibility of the controller layer is to take user input, call model
methods to determine what to do based on the input, pass the output of those
methods to the view and finally take the response body and metadata from the
view and send it back to the web server.

Resources:
https://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/
https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/
http://guides.rubyonrails.org/action_controller_overview.html
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
The router determines which controller the user’s request should be sent to.

Resources:
https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/
http://guides.rubyonrails.org/routing.html
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
The client makes a GET request, that request is sent to the web server which
uses routes to determine which controller to send the request to.  The
controller parses the request and asks the model to get the requested resource.
 The model communicates to the database and performs the business logic to
 retrieve that resource and sends it back to the controller.  The controller
 then sends the resource to the view which generates whatever it is the user
 should see based on the resource and then passes it back to the controller
 again. The controller then sends the response body to the web server which 
 turns it into a valid HTTP response to the user.

Resources:
https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/
```
