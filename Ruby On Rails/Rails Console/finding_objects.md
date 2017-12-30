```User.find_by_email("usertest2@test.com")```

```Genre.pluck(:name)```

```Blog.find_by_slug('my-blog-post-4')```

```Book.order('sales DESC').first```

```Book.order('sales DESC')```


```Book.maximum(:sales)```

```Book.average(:sales).to_f```

```.sum(:sales)```

```.any?```

```Book.where(title: "The Force").author```

```Book.find_by_sql("")```

```Book.find_by_title("The Force").class```

```Book.find_by_title("The Force")```

```.find_each(&:save)```

