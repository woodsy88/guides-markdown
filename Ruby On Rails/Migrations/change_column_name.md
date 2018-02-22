create a migration to change the column name of overtime_requests to a new name of ```daiy hours```

```rails g migration add_daily_hours_to_posts```

open migration file

then use the ```rename_column```

```
class AddDailyHoursToPosts < ActiveRecord::Migration[5.1]
  def change
    rename_column :posts, :overtime_request, :daily_hours
  end
end
```

udemy video

https://www.udemy.com/professional-ruby-on-rails-coding-course/learn/v4/t/lecture/5665138?start=0
