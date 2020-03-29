# README sample_app
We are following Michael Hartl's Ruby on Rails Tutorial, 4th ed.
Some issues arise because I am using later versions of ruby, rails and modules
than described in the tutorial, and some things don't work exactly the same.

**Note: only files that were manually changed are being checked in**
Files automatically created by rails utilities are not present in the repository.

* Ruby version: ruby 2.6.3p62

* Rails version: 6.0.2.2

* System dependencies: Ubuntu 18.04 LTS desktop 64 bit

## How to recreate sample_app
Here is a list of operations that should build sample_app in a fresh installation.
Assuming some workspace in which the operations are executed, e.g. ~/wkspc/.
1. $ git clone git@github:dmrmoney/railsapps.git (or download from github)
1. $ rails new sample_app --skip-git # this will create a default app, including a Gemfiile
1. $ cd sample_app
1. $ git checkout -- Gemfile # or copy sample_app/Gemfile from github onto existing Gemfile
1. $ bundle install
1. $ bundle update
1. $ rails test # it should succeed, but with 0 tests.
1. $ rails server # firefox: localhost:3000 should show "Yay! Rails page

Create "Home" and "Help" static pages using a generator
1. $ rails generate controller StaticPages home help
1. Manually add a third static "About" page app/views/static_pages/about.html.erb. 
1. Add related code to test/controllers/static_pages_controller_test.rb, config/routes.rb, app/controllers/static_pages_controller.rb. 
1. The related code is checked in, either copy manually or use git checkout -- filenames
1. $ rails test --> should verify 6 assertions.






