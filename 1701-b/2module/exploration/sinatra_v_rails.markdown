## Sinatra versus Rails Exploration

### Setup:

First, clone down the Rails project:

```terminal
git clone https://github.com/turingschool/job-tracker.git rails_project
```

And then clone down the Sinatra project:

```terminal
git clone https://github.com/turingschool/bike-share.git sinatra_project
```
Now cd into each project, run `bundle` on each project, and you're ready to go. We will only be looking at the code base and not interacting with the app. If you wanted to run the server and interact with the app, you would need to create your database, migrate your migrations, etc.

### Exercise:

1. Take a look at this stripped down Sinatra app and this stripped down Rails app. How are they different and how are they similar? Identify 5 differences, and for each one describe 1-2 implications. What effect does that difference have for each framework? If you don't know exactly, draw on your knowledge and experience and make some educated guesses/inferences. Also, practice your research skills to look into the differences.

  * Sinatra: i. Only has one controller file, ii. Only has a Model, Views, and Controller directory (MVC), iii. Within the app file the paths are specified with the url (eg: get "/stations'"), v. for testing we have model and feature tests, it also looks like there is a controller directory within the spec directory

  * Rails: i. 3 controller files, ii. in addition to the MVC directories also has a "mailers" and "helpers" directory, iii. Within the app file paths are specified with words taken from the CRUD process (eg: create, update, etc.), iv. Has a bin, lib, and vendor directory, v. again, we will have model tests and feature test, it looks like rails tests require a spec helper and a rails helper file.
,
1. Consulting blogs and commentary you find online, identify 3 similarities between Rails and Sinatra.
  * Both employ the MVC framework
  * Both are Ruby frameworks


1. Consulting blogs and commentary you find online, identify 3 things that distinguish Rails, advantages.

  * "Rails is used for larger scale applications, anything with an expectancy for many users and many end points (or places where the application can be accessed, like a URL or login portal). Sinatra is for small projects and API pullers, something that has just a few or some limited number of users and fewer end points".

  * Rails works better with database, while Sinatra is preferred when pulling data from an API.

  * Rails is better for "full scale applications". However, for a simpler application Sinatra would better and Rails would be overkill.

  * Rails and Sinatra "are solving a different set of issues, even though they indeed overlap. While Rails is a framework focused on writing model driven web applications, Sinatra is a library for dealing with HTTP from the server side. If you think in terms of HTTP requests/responses, Sinatra is the ideal tool. If you need full integration and as much boilerplate as possible, Rails is the way to go".

  * A potential weakness to Sinatra is security... Sinatra leaves many common attack vectors open that the developer needs to be aware of and deal with. Rails offers built-in security  

1. In your Rails project, what does the `routes.rb` file inside of the `/config` directory do? What does this correlate to in our Sinatra app?
    * In Rails the 'routes.rb" file is mapping out the HTTP verbs, which, in Sinatra is done directly in the controller.

1. We teach Sinatra by adding some structures that Sinatra doesn’t need, but help you make the transition between Sinatra and Rails. What does a stripped down implementation of Sinatra look like, and what are the pieces we’ve added for educational purposes?
  * It does not need a database; we added that...
