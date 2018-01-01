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