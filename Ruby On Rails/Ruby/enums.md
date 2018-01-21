creating an enum in a model

```ruby
class Post < AuditLog
  enum status: { pending: 0, confirmed: 1, rejected: 2 }
end```

##TEsing a enum in the rails console

Change the enum to confirmed

```AuditLog.first.confirmed!```
