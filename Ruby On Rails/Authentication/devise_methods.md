## Devise Methods - VIEWS

**User Signed**

```<% if user_signed_in? %>
      perform this block is user signed in
<% else # user not signed it %>
      else this block if user not signed in
<% end # if user is signed it %>```

```sign_in``` method is one of the Devise helper methods.


Current User

```<% if current_user %>```



## Devise methods

```user_id: User.last.id```


## controllers

by putting the below line in any controller it will require an autheticated user for it

```before_action :authenticate_user!```
