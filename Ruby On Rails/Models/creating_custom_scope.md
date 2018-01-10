## Custom Scope in the Model that passes specific data to the controller

We want to show current_user only their posts in the ```index view```. We currently have this logic in the controller. Lets refactor it into the model.

in ```post.rb``` create a custom scope

```ruby
  scope :posts_by, ->(user) { where(user_id: user.id) }
```

>this scope takes user as an argument/param

In ```posts_controller.rb``` remove the logic and replace with our scoped model method ```posts_by``` from above.

replace the current

```ruby
def index
  @posts = current_user.posts
end
```

with the new scope method

```ruby
def index
  @posts = Post.posts_by current_user
end
```

>notice how it takes current_user as the argument/param set in the custom scope in ```post.rb```
