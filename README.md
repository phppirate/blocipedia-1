README.md

BY: Vaun Podlogar

Blocipedia Application

Create with my Mentor during bloc.io apprenticeship program


http://gentle-spire-4433.herokuapp.com/


***********   Purpose

Build an application that allows users to create public and private Markdown-based wikis. We'll call our application "Blocipedia", but you're free to name it anything you want.


***********   Use Case 

Wikis are a great way to collaborate on community-sourced content. Whether the wiki is for a hobby or work-related project, we'll build an app that lets users create their own wikis and share them publicly or privately with other collaborators.


Components

**********  Devise start

Devise gem for authentication. Blocipedia's authentication system should allow users to sign up, sign in, reset their passwords and send emails for account authorization.

Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { :host => 'localhost:3000' }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root :to => "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

  4. If you are deploying on Heroku with Rails 3.2 only, you may want to set:

       config.assets.initialize_on_precompile = false

     On config/application.rb forcing your application to not access the DB
     or load models when precompiling your assets.

  5. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

********** Devise end







Marked gem to create a live markdown editor so that users can see their Markdown converted in real-time.

Redcarpet gem to parse Markdown syntax.

Stripe gem so that you can charge users for creating premium accounts (for creating private wikis). 

Friendly ID gem to create readable URLs. 

Bootstrap 3 to style Blocipedia. Bootstrap will provide the basic CSS classes needed to make Blocipedia look nice.

***********   User Stories

 1. As a user, I should be able to sign up for a free account by providing a user name, password and email address.

2. As a user, I want to be able to sign in and out of the Blocipedia.

3. As a user, I want to be able to create wiki pages using Markdown syntax.

4. As a user, I should see my Markdown syntax rendered in real-time, so that I can easily validate the format of my wiki.

5. As a user with a free account, I want to be able to create public wikis that anyone may view.

6. As an user I want to be able to upgrade my account from a free plan to a paid (premium) plan so that I can create private wikis.

7. As a user with a premium account, I want to be able to create private wikis that require a Blocipedia account and proper authorization to view.

8. As a user with a premium account, I want to be able to add collaborators to my private wikis.
As a user with a premium account, I should be able to add an unlimited number of collaborators to my wikis.
