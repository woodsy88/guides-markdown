### Goal of model:
- Keep track of employee overtime

### Dependencies (which other models is it associated with)
- User

### Attributes (what columns with the model need)
- status:integer (enum) -> pending, complete
- start_date:date -> default previous monday
-date_verified:date

Once you have above information worked out then you write the generator

Generator to use
```rails g resource AuditLog user:references status:integer start_date:date end_date:date```
