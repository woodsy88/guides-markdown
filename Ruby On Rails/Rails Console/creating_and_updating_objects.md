## Create

```Blog.create!(title: "Baseball", body: "farts and stuff")```

creating a new class with a reference to another model

```Technology.create!(name: "Rails", portfolio_id: Portfolio.last.id)```

```portfolio_item_2``` is a variable holding a singlular Portfolio. A portfolio has many technologies. This creates a new technology assosciated with ```portfolio_item_2```

```portfolio_item_2.technologies.create!(name: "React")```

```Portfolio.create!(title: "Web App 1", subtitle: "anything", body: "stuff and stuff", technologies_attributes: [{name: "Ruby"},{name: "Rails"},{name: "Java"}])```

```ruby
u = User.last
b = Blog.last
Comment.create!(user_id: u.id, blog_id: b.id, content: "Some COntent")
```

## Update

```u.update!(name: "Cher")```

```user.update!(roles: "site_admin")```



