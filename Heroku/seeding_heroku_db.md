## To seed your heroku db with data from your seeds file

run:

```heroku run rake db:migrate```

to update the schema, and then run:

```heroku run rake db:seed```

That would integrate all of the data.

----------


## Clean out DB and re-seed database on heroku

Since heroku doesn't allow for destructive commands, such as:

```heroku run rake db:setup```

You will need to use alternative commands, the equivalent commands are:

Delete Seed Data

```heroku pg:reset```

The re-Seed Data

```heroku run rake db:migrate```

```heroku run rake db:seed```
