## Resource generator

Generates Model, Controller, but no views

```rails g resource Post date:date rationale:text```

```rails g resource Portfolio title:string subtitle:string body:text main_image:text thumb_image:text```

With a reference to user and blog table

```rails g resource Comment content:text user:references blog:references```

Generate a model with user reference and 2 date attributes with a status attribute that is an integer and an enum

```rails g resource AuditLog user:references status:integer start_date:date end_date:date```


## Controller Generators

Generates controller and corresponding views

Generates Controller, with 3 empty methods inside and the corresponding view files

```rails g controller Pages home about contact```




## Model Generators

Generates just the model

```rails g model Skill title:string percent:integer```

Generates Model with belongs_to association to another model

```rails g model Technology name:string portfolio:references```

create just a model

```rails g model post```

## Scaffoldings

Generates Model, Controller, Views and tests

```rails g scaffold Blog title:string body:text```




## Deleting a generator if made by mistake

```rails d controller welcome -p```
