# Sinatra From Scratch

## Overview

We'll cover the components of a basic Sinatra application and how to create a local host server to view the application in the browser.

## Objectives

1. Review gems and how to keep them updated using `bundle install`
2. Describe the purpose of the application controller and `app.rb` in Sinatra
3. Run a Sinatra app by entering `rackup app.rb` in your terminal 

## Basic Sinatra App

### Sinatra Gem

This is not a lab, as there's nothing for you to submit. But to follow along with the lesson, make sure you fork and clone this repository. 

It's important to note that Sinatra is just a gem. It's a library of code that developers wrote to allow us to build light-weight web applications quickly. If you take a look at our `Gemfile` (a list of all the gems our application uses), you will see the Sinatra gem listed.

The first thing you need to do is enter in terminal `bundle install`. Just like software has different versions that require you to update your mobile apps, gems have newer versions. `bundle install` will lock in the current versions of the gems for your application, that way if any updates happen, your app won't break. It keeps the versions locked in a file called `Gemfile.lock` that is created for you.

### `app.rb`

The `app.rb` file is the heart and soul of a Sinatra application. This is our application controller. The application controller handles all incoming requests to our app, and sends back the appropriate responses to the client.

The first line of `app.rb` is just requiring the Sinatra gem so that we can incorporate its functionality.

On the next line, we define a class `App` and have it inherit from `Sinatra::Base`. This way, any instance of our class App will have all the functionality of the Sinatra class.

Inside our class we have a Sinatra method define, or controller action. This method responds to a `GET` request to the root url and displays the text `Hello, World!` in the browser.


### Starting The App

To actually check if our app is working in the browser, enter `rackup app.rb` in your terminal. 

Sinatra relies on Rack for its middleware. Because we have the Sinatra gem listed in our Gemfile, we automatically have the Rack middleware setup.

Once your server is running, visit `localhost:9292` in the browser to see `Hello, World!` displayed.


<p data-visibility='hidden'>View <a href='https://learn.co/lessons/sinatra-from-scratch-readme' title='Sinatra From Scratch'>Sinatra From Scratch</a> on Learn.co and start learning to code for free.</p>
