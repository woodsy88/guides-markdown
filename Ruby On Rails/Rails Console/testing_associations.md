## Checking associations afer creating new model

I Created a new model called ```AuditLog``` that ```belongs_to``` a ```user```

I want to test out its association with user

first add to ```user.rb``` ```has_many :audit_logs``` and ensure ```audit_log.rb``` has ```belongs_to :user```

Then open up test rails console ```rails c --sandbox```

then create new AuditLog

```AuditLog.create(user_id: User.last.id)```

>you may need to check your validations and add all attributes if needed

then to test users association with the audit log

```User.last.audit_logs```

then to test the audit logs association with the user

```AuditLog.last.user```
