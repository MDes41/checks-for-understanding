## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
  - Cookies are small information that can be passed along with response request
  cycles to store data between static pages.
* What’s the difference between a session and a cookie?
  - Session is a type of cookie that remains active throughout the cycle of the
  session, where cookies are different
* What’s a flash and when do you want to use flashes?
  - flashes are a type of cookie that occur once and then delete, used to notify
  the user
* Why do people say “HTTP is stateless”?
  - Because nothing is keeping the cylce open, it is request response of
  static pages.  Not open connection is open.
* What’s authentication? Explain.
  - Authentication is a method BCrypt uses to decode your password digest
* What’s the difference between authentication and authorization?
  - Authentication lets the user into the session with a password, but authorization is stored in the database to users that allows different privileges
* What’s a before filter?
 - Runs the method after the before filter on all controller methods before the action on the controller takes place.
* How do we keep track of a user once they’ve logged in?
  - Not to sure, I assume through the routes
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  - Not to sure
* At a high level, what tools can you use to implement authorization? How would you use them?
  - Controllers, or enums, sessions, or cookies.  You could
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  - integer role, and you declare them on the model
* What are some strategies you can use to keep your views DRY?
  - partials and helper methods 
