We have a factory

```ruby
FactoryGirl.define do
  factory :audit_log do
    user
    status 0
    start_date (Date.today - 6.days)
    end_date "2018-01-13"
  end
end
```

We want to test if it works

run ```rails console --sandbox```

then run this

```AuditLog.create!(user_id: User.last.id, status: 0, start_date: (Date.today - 6.days))```

----

Now to test if a factory works in console

run ```rails c -e test```

then run ```FactoryGirl.create(:audit_log)```
