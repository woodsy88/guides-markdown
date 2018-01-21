
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


## Bye Bug Commands

go to next line while pasued using byebug

```next```

completely unpauses the code

```continue```

https://github.com/deivid-rodriguez/byebug/blob/master/GUIDE.md#command-help

## using byebug in rspec tests

add byebug to your test

```ruby
    it 'renders audit log content' do
      visit audit_logs_path
      byebug
      expect(page).to have_content(//)
    end
  ```

then run the test ```rspec spec/features/audit_log_spec.rb rspec spec/features/audit_log_spec.rb```

byebug will stop test

## test commands - when using byebug in test files

```current_path```

