## Creating a helper to show certain nav links to a signed in user and certain nav links to an unsigned in user


We have a nav bar view with too much logic in it (the if else statements). Below is the example

```html
<!-- Collect the nav links, forms, and other content for toggling -->
  <div class="collapse navbar-collapse navbar-right" id="navbar-collapsible-content">
    <ul class="nav navbar-nav ">
   <% if user_signed_in? %>
     <li class="dropdown pc-menu">
       <a id="user-settings" class="dropdown-toggle" data-toggle="dropdown" href="#">
         <span id="user-name"><%= current_user.name %></span>
         <span class="caret"></span>
       </a>
       <ul class="dropdown-menu" role="menu">
         <li><%= link_to 'Edit Profile', edit_user_registration_path %></li>
         <li><%= link_to 'Log out', destroy_user_session_path, method: :delete %></li>
       </ul>
     </li>
     <li class="mobile-menu">
       <%= link_to 'Edit Profile', edit_user_registration_path %>
     </li>
     <li class="mobile-menu">
        <%= link_to 'Log out', destroy_user_session_path, method: :delete %>
      </li>

    <% else # user not signed it %>
      <li ><%= link_to 'Login', login_path %></li>
      <li ><%= link_to 'Signup', signup_path %></li>
    <% end # if user is signed it %>
    <%= render collapsible_links_partial_path %>
    </ul>
  </div><!-- navbar-collapse -->
  ```

Create a new directory to hold the 2 partials you are going to split the logic from the view (nav bar) into. For this example we will create a collapsible_elements directory inside the ```navigation directory``` in the views.

```app/views/layouts/navigation/collapsible_elements```

Inside the directory create two files: ```_signed_in_links.html.erb``` and ```_non_signed_in_links.html.erb```. Now cut the content from ```_collapsible_elements.html.erb``` file’s if else statements and paste it to the corresponding partials. The partials should look like this:

```_signed_in_links.html.erb```

```html
<li class="dropdown pc-menu">
  <a id="user-settings" class="dropdown-toggle" data-toggle="dropdown" href="#">
    <span id="user-name"><%= current_user.name %></span>
    <span class="caret"></span>
  </a>

  <ul class="dropdown-menu" role="menu">
    <li><%= link_to 'Edit Profile', edit_user_registration_path %></li>
    <li><%= link_to 'Log out', destroy_user_session_path, method: :delete %></li>
  </ul>
</li>

<li class="mobile-menu">
  <%= link_to 'Edit Profile', edit_user_registration_path %>
</li>
<li class="mobile-menu">
  <%= link_to 'Log out', destroy_user_session_path, method: :delete %>
</li>
```

```_non_signed_in_links.html.erb```

```html
<li ><%= link_to 'Login', login_path %></li>
<li ><%= link_to 'Signup', signup_path %></li>
```

Now inside the ```_collapsible_elements.html.erb file```, instead of if else statements, add the ```render``` method with the ```collapsible_links_partial_pathhelper``` method as an argument. The file should look like this


```html
<div class="collapse navbar-collapse navbar-right" id="navbar-collapsible-content">
  <ul class="nav navbar-nav ">
    <%= render collapsible_links_partial_path %>
  </ul>
</div>>
```                                    


```collapsible_links_partial_path``` is the method we are going to define inside the ```NavigationHelper```. Open or Create ```navigation_helper.rb``` in the helpers directory


and define the method inside the module. The navigation_helper.rb file should look like this:

```ruby
module NavigationHelper

  def collapsible_links_partial_path
    if user_signed_in?
      'layouts/navigation/collapsible_elements/signed_in_links'
    else
      'layouts/navigation/collapsible_elements/non_signed_in_links'
    end
  end
  
end
```

> Make sure the file paths are correct for the desired partials                

The ```collapsible_links_partial_path```  - If a user is signed in, return a corresponding partial’s path. If a user is not signed in, return another partial’s path.

Make sure you import NavigationHelper into the ```ApplicationHelper``` file

```ruby
require 'navigation_helper.rb'

module ApplicationHelper
  include NavigationHelper
end
```


**Repositiry Links**

[Colllabfield Branch](https://www.google.com))

