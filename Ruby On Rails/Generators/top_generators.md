## Resource generator
Generates Model, Controller, but no views

```rails g resource Post date:date rationale:text```

```rails g resource Portfolio title:string subtitle:string body:text main_image:text thumb_image:text```

Generates Model, Controller, but no views - with a reference to user and blog table
```rails g resource Comment content:text user:references blog:references```


## Controller Generators
Generates controller and corresponding views

Generate Controller with 3 empty methods inside and corresponding view files
```rails g controller Pages home about contact```


## Model Generators
Generates just the model

```rails g model Skill title:string percent:integer```

Generates Model with belongs_to association to other model
```rails g model Technology name:string portfolio:references```


## Scaffoldings
Generates Model, Controller, Views and tests

```rails g scaffold Blog title:string body:text```


## Deleting a generator if made by mistake

```rails d controller welcome -p```