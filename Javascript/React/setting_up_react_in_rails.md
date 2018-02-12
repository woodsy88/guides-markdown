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

to test are setup

