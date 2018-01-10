
run the commands to drop and create the database, and run migrations

```
rails db:drop
rails db:create
rails db:migrate

```

rollback the last migration

```rails db:rollback```

If you want to rollback a specific migration with a version you should do:

```rake db:migrate:down VERSION=YOUR_MIGRATION_VERSION```
