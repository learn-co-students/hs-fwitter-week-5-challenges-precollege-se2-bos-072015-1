## Day 5 Challenges!

+ Finish up today's ToDo.
+ Move your sign up and sign in forms from the users page to a new sign in page.
+ Set up your application to display EITHER a "Sign In" or "Sign Out" link at the top of the page - depending on whether the user is signed in or not.
  * Hint: You’ll need to use Ruby if/else statements with erb tags - similar to what we did when we hid the tweets form.

### Bonus Challenges:
+ Sinatra has a nice feature called `helpers` for creating methods that can be used throughout your application (not just in one view or route). For instance, you might create a `signed_in?` method that returns true if a `session[:user_id]` exists. This method could be used in your view like this:

```erb
<% if signed_in? %>
  <h3>Add a tweet</h3>
  <form action="/tweets" method="POST">
  ...
  </form>
<% else %>
  ...
<% end %>
```

This syntax makes it a little easier for collaborators to follow the logic of your code.

To use Sinatra helpers, add a `helpers` code block to your application controller and write your helper methods inside of that code block. Like this:

```ruby
class ApplicationController < Sinatra::Base

  helpers do
    # create your own helper methods here
  end

end
```

You can read more about helpers in the Sinatra documentation here: http://www.sinatrarb.com/intro.html#Helpers

  * Your first challenge is to create a helper method called `current_user` that finds a user based on their session ID. Then use this helper method to display “Welcome, <user’s name>!” at the top of every page if a user is signed in.

  * Your second challenges is to add an `error` helper method that tracks session[:errors]. Set up your sign in page to display an error if a user tries to log in before they have signed up. Don’t forget to delete this error message if the user signs in successfully.
