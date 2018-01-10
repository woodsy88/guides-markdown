## Creating a .ENV File to store secure credentials

The .env file is where you put all your credentials you want to be private

First you need the dotenv gem. Add to gem file

```gem 'dotenv-rails', :groups => [:development, :test]```

Then you need to create the actual .env file. run ```touch .env``` from the root directory of your project

Now before we can use this file let's make sure that we add it to the gitignore file so that our credentials don't get checked into source control. At the end of the git ignore file add this code:

```
/.env
```

We can verify that this is working by running git status and our .env file shouldn't show up

Dev Camp Guide

https://rails.devcamp.com/rest-microservices/sms-messages/securing-credentials-in-a-rails-app-with-dotenv
