```Blog.create!(title: "Baseball", body: "farts and stuff")```

```Technology.create!(name: "Rails", portfolio_id: Portfolio.last.id)```

```p2.technologies.create!(name: "React")```

```Portfolio.create!(title: "Web App 1", subtitle: "anything", body: "stuff and stuff", technologies_attributes: [{name: "Ruby"},{name: "Rails"},{name: "Java"}])```

```u.update!(name: "Cher")```

```user.update!(roles: "site_admin")```

```ruby
u = User.last
b = Blog.last
Comment.create!(user_id: u.id, blog_id: b.id, content: "Some COntent")
```

