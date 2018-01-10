creating an enum in a model

```ruby
class Post < ApplicationRecord
  enum status: { submitted: 0, approved: 1, rejected: 2 }
end```

