Open the Gemfile and add those gems to the test group

```ruby
gem 'rspec-rails', '~> 3.6'
gem 'factory_girl_rails'
gem 'rails-controller-testing'
gem 'headless'
gem 'capybara'
gem 'poltergeist'
gem 'database_cleaner'
```

```rspec gem``` is a testing framework

```factory_girl``` is for adding sample data

```capybara``` is for simulating a user’s interaction with the app

```poltergeist``` driver gives the JavaScript support for your tests.


```headless gem``` is required to support headless drivers. poltergeist is a headless driver, that’s why we need this gem. 

```rails-controller-testing gem``` is going to be required when we will test requests and responses with the requests specs.


```database_cleaner``` is required to clean the test database after tests where JavaScript was executed. Normally the test database cleans itself after each test, but when you test features which has some JavaScript, the database doesn’t clean itself automatically.



