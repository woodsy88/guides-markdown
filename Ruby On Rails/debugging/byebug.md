
## Running Byebug in tests

insert ```byebug``` into block of code in your tests

then run the test just for that file

when the test pauses, enter the values you want to know

**Example:**

```ruby
it 'has an overtime request greater then 0.0' do
      @post.overtime_request = 0.0
      byebug
    end
```

then you can check what ```@post.overtime_request```, ```@post``` holds in the console
