## Lib Directory

sits outside the rest of the core application

it can be treated like a helper module, or a gem



## Creating a module

first open up ```config/application.rb```

add a new config block

```config.autoload_paths << Rails.root.join("lib")```

This essentially adds the lib directory to the app


Using LIB video from profesional rails course
https://www.udemy.com/professional-ruby-on-rails-coding-course/learn/v4/t/lecture/5490226?start=0
