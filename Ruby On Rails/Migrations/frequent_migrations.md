
Adding an enum to posts model

```rails g migration add_status_to_posts status:integer```

adds a user_id column to posts

```rails g migration add_users_to_posts user:references```


Adds a foreign key to blogs table for topics

```rails g migration add_topic_reference_to_blogs topic:references```

Add new column to table

```rails g migration add_badge_to_skills badge:text```

Add slug col to blog table of type string that has to be unique

```rails g migration add_slug_to_blogs slug:string:uniq```

```rails g migration add_slug_to_topics slug:string```

Add a column called overtime_request to the posts table of the type decimal

```rails g migration add_post_hour_request_to_posts overtime_request:decimal```


Add a column called phone number to users that takes type string

```rails g migration add_phone_to_users phone:string```
