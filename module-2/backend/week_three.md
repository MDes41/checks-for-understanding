## Week Three Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What are the 3 main features in an ERD?
  * The three main features in an ERD, Entity Relationship Diagrams, are the entity or table representation, the relationship to another entity or table representation, and the attribute of the entity or table representation.
2. Create an ERD for the following database: Restaurants, Customers, Items, Ingredients, Beverages, Orders, Vendors.
  * see attachment
3. What is the entry at the command line to create a new rails app?
  * rails new <NAME> <OPTIONS> example (rails new my_app -d postgresql)
4. What do Models generally inherit from in rails?
  * Models generally inherit from ActiveRecord::Base (may be different in rails 5)
5. What do Controllers generally inherit from in a rails project?
  * Controller generally inherit from ApplicationController
6. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  * `get "/horses/:id", to: "horses#show"` or `resources :horses, only: [:show]`
7. What rake task is useful when looking at routes, and what information does it give you?
  * `rake routes` tells us the prefix, or helper method for a path, the verb, the URI path, the method, and controller the route has
8. What is an example of a route helper? When would you use them?
  * You would use a route helper usually when defining a link and what path the link takes, or in the controller to redirect to a certain page.  An example would be horses_path or horse_path(horse.id) or new_horse_url or edit_horse_url
9. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  * The difference between the two are that path is just the short path like /horses/1 and the url give the entire link like http://www.my_app.com/horses/1, and usually the path is prefered if you can use either
10. What are strong params and why are the necessary?
  * Strong params are set in a private method on the controller to only permit certain key values in the params hash.  This is necessary so that nobody can add to the html form from the client side and pass extra params into a form causing a potential hack or corupt information into the app.
11. What role does `form_for` play in helping us create our forms?
  * I am assuming it is a helper method to create forms, but don't know many other ways to create forms unless you use form tag which requires more inputs to function, but is more customizable.  Form for lets us call the ivar to create a table which is very convenient.   
12. How does `form_for` know where to submit the user's input?
  * Rails is smart enough to know based on what view it is rendered in.  
13. Create a form using a `form_for` helper to create a new `Horse`.

  ```
  <%= form_for @horse do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>
    <%= f.submit %>
  <% end %>
  ```
14. Why do we want to validate our models?
  * We want to validate the model so that we are in control of what information is put into the database or we would create a bunch of junk data without checks to make sure the user is putting the data in the fields correctly
