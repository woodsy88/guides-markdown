
## 1. Adding Using react-rails Gem

add gem to gem file

```gem 'react-rails'```

then run generator

```rails g react:install```

which creates the files:

```
      create  app/assets/javascripts/components
      create  app/assets/javascripts/components/.gitkeep
      insert  app/assets/javascripts/application.js
      create  app/assets/javascripts/components.js
      create  app/assets/javascripts/server_rendering.js
      create  config/initializers/react_server_rendering.rb
```


----------

generate a component with es6 syntax

>react-rails now fully supports es6, no need to add es6 in the file name, but if you use it in the generator then it creates the file with es6 layout

```rails generate react:component Label label:string --es6```

which creates

```create  app/assets/javascripts/components/label.es6.jsx```

then add to view

```<%= react_component 'Label', label: 'Select title' %>```

react_rails gem
https://rubygems.org/gems/react-rails
https://github.com/reactjs/react-rails

------



If you’re using Rails 5.1 or higher, you can directly create a new app with React support out of the box simply by running:

```rails new myapp --webpack=react```

https://hackernoon.com/how-to-get-your-rails-data-into-your-react-component-with-webpacker-647dc63706c9
