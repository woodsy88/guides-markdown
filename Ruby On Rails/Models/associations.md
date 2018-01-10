
Setting an association to optional

```belongs_to :user, optional: true```


------

has_many associations with destroy. The ```dependent: :destroy``` argument says, when a user gets deleted, all posts what the user has created will be deleted too.

```ruby
class User < ApplicationRecord
  has_many :posts, dependent: :destroy
end
```

when you set a has_many in 1 model, you need to set a belongs_to in the corressponding model

```ruby
class Post < ApplicationRecord
  belongs_to :user
end
```

---------

