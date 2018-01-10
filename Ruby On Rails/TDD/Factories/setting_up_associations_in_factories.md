```ruby
FactoryGirl.define do
  factory :post do
    title 'a' * 20
    content 'a' * 20
    user
    category
  end
end
```

it’s very easy to set up an association for factories. All we had to do to set up ```user``` and ```category``` associations for the ```post``` factory, is to write factories’ names inside the post factory.
