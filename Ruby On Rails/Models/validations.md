adding a validation to ensure a number entered into the db is greater then a set value

```validates :overtime_request, numericality: { greater_than: 0.0 }```

validates the presence of a value - you must enter the value for the record to be submitted to the database

```validates_presence_of :date, :rationale, :overtime_request```


```validates_uniqueness_of :name```

```validates_presence_of :name```
