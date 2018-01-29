schema

```t.integer "status", default: 0```

creating an enum in a model

```ruby
class Post < AuditLog
  enum status: { submitted: 0, confirmed: 1, rejected: 2 }
end```

##Testing a enum in the rails console

Change the enum to confirmed

```AuditLog.first.confirmed!```

in the controller

```ruby
  def homepage
    @pending_approvals = Post.where(status: 'submitted')
  end
```

or


```ruby
  def homepage
    @pending_approvals = Post.submitted
  end
```
