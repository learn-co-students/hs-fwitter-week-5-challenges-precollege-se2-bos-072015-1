---
tags: forms, kids, ruby, advanced, challenges
language: ruby
level: 2
type: challenges
---

## Week 5 Challenges!

+ Move your sign up and sign in forms from the users page to a new sign in page.
+ Set up your application to display EITHER a Sign In or Sign Out link at the top of the page - depending on whether the user is signed in or not. 
  * Hint: You’ll need to use Ruby if/else statements with erb tags - similar to what we did when we hid the tweets form.

### Bonus Challenges: 
+ Sinatra has a nice feature called `helpers` that you can use to write methods that are available for every route in your application controller. To use Sinatra helpers, add a `helpers` code block to your application controller, like this:

```ruby
class ApplicationController < Sinatra::Base

  helpers do
    # create your own helper methods here 
  end

end
```

And write your helpers methods inside of that code block. You can read more about helpers in the Sinatra documentation here: http://www.sinatrarb.com/intro.html#Helpers 

  * Your first challenge is to create a helper method called `current_user` that finds a user based on their session ID. This helper method should help you to display “Welcome, <user’s name>!” at the top of every page when they are signed in.

  * Your second challenges is to add an `error` helper method that tracks session[:errors] and set up your sign in page to display an error if a user tries to log in before they have signed up. Don’t forget to delete this error message if the user signs in successfully.
