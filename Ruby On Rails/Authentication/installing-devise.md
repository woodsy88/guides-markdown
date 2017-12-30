Add to your Gemfile

```
gem 'devise' 
```

Then run commands

```bundle install```

then

```rails generate devise:install```

## Creating a User Model With a Devise Generator

Now let’s use a devise generator to create a User model.

```rails generate devise User```

Initialize a database for the app by running:

```rails db:create```

Then run this command to create new tables in your database:

```rails db:migrate```

> By installing Devise gem, we not only get the back-end functionality, but also default views. If you list your routes by running: rails routes

## Generating Devise Views Directory

If you look at the views directory, you see that there isn’t any Devise directory by default, which we could modify. In order to modify Devise views, we’ve need to generate the directory with a devise generator. Run

```rails generate devise:views```