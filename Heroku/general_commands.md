```heroku logs -n 250```

```heroku run rails c```


```heroku logs```

```heroku pg:reset DATABASE```

restarts the server, good idea whenever you do any big changes to the production db

```heroku restart```

```heroku run rake db:migrate```

```heroku --v```

```heroku config:set TWITTER_CONSUMER_KEY=KEY_NUMBER```

```heroku config```

--------

## Setting up new heroku app

Create new heroku app

```heroku create app-name```

Push code from master to heroku

>Make sure that you have commited and pushed all changes up to your remote master

Push code up to heroku

```git push heroku master```

>after first push you can just use ```git push heroku```


-------


##To seed your heroku db with data from your seeds file

run:

```heroku run rake db:migrate```

to update the schema, and then run:

```heroku run rake db:seed```

That would integrate all of the data.

----------


Check if your connected to heroku

```git remote -v```


Open your newly created app

```heroku open```


---------

## Clean out DB and re-seed database on heroku

Since heroku doesn't allow for destructive commands, such as:

```heroku run rake db:setup```

You will need to use alternative commands, the equivalent commands are:

Delete Seed Data

```heroku pg:reset```

The re-Seed Data

```heroku run rake db:migrate```

```heroku run rake db:seed```
