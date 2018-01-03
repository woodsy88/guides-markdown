## How to setup Rspec

Add rspec gem to test group in gem file

```
group :development, :test do
  gem 'rspec-rails', '~> 3.6'
end
```

To initialize the spec directory for the RSpec framework run the following:

```rails generate rspec:install```


``spec`` means a single test in RSpec framework. When we run our specs, it means that we run our tests.

If you look inside the app directory, you will notice a new directory called ``spec``. This is where we’re going to write tests. Also you may have noticed a directory called ``test``. This is where tests are stored when you use a default testing configuration. We won’t use this directory at all. You can simply remove it from the project.