## What is a helper

Rails views is not the right place for logic

We’ll extract logic from Rails views and put it inside the helpers directory.

## Creating a helper

navigate to ```app/helpers```

create a new file

```navigation_helper.rb```

Inside helper files, helpers are defined as modules. Inside the navigation_helper.rb define the module

```ruby
module NavigationHelper
end
```


## Restricting helpers to their corresponding controllers only

By default Rails loads all helper files to all views. Personally I do not like this, because methods’ names from different helper files might clash. To override this default behavior open the ```application.rb``` file

```config/application.rb```

Inside the Application class add this configuration

```config.action_controller.include_all_helpers = false```

Now helpers are available for corresponding controller’s views only. So if we have the PagesController, all helpers inside the pages_helper.rb file will be available to all view files inside the pages directory

## Injecting Helper files into ApplicationHelper so it is available across thelets entire app

**If you dont have a controller that corresponds to a view**

include the ```NavigationHelper``` module inside the ```ApplicationHelper```

Inside the ```application_helper.rb``` file, require the ```navigation_helper.rb``` file. Now we have an access to the ```navigation_helper.rb``` file’s content. So let’s inject ```NavigationHelper``` module inside the ```ApplicationHelper``` module by using an include method. The ```application_helper.rb``` should look like this:

```ruby

require 'navigation_helper.rb'

module ApplicationHelper
  include NavigationHelper
end


```

Now ```NavigationHelper``` helper methods are available across the whole app.

## Splitting logic from views into helpers

take the html that is inbetween the logic and split it into new files


**render the helper in the view**

<%= render helper_method_name %>
