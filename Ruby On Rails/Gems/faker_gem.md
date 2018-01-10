## Faker Gem

The faker gem is used to generate dummy text. Mostly used in seed files

## Installing Faker

Add faker gem to your Gemfile

```gem 'faker'```

and

```bundle install```


## Using in seed file

```ruby
def seed_posts
  categories = Category.all

  categories.each do |category|
    5.times do
      Post.create(
        title: Faker::Lorem.sentences[0],
        content: Faker::Lorem.sentences[0],
        user_id: rand(1..9),
        category_id: category.id
      )
    end
  end
end
```
