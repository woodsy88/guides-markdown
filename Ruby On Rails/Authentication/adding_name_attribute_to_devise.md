### Adding a name attribute at the start of the app

Navigate to db/migrate and open the ```CREATION_DATE_devise_create_users.rb``` file and add ```t.string :name, null: false, default: ""``` inside the create_table method.


Now run the commands to drop and create the database, and run migrations.

```
rails db:drop
rails db:create
rails db:migrate
```


To be able to send an extra attribute, so the Devise controller would accept it, we’ve to do some changes at the controller level. We can do changes to Devise controllers in few different ways. We can use devise generator and generate controllers. Or we can create a new file, specify the controller and the methods that we want to modify. Both ways are good. We are going to use the latter one.

Navigate to **app/controllers** and create a new file ```registrations_controller.rb```. Add the following code to the file:

```ruby

class RegistrationsController < Devise::RegistrationsController

  private

  def sign_up_params
    params.require(:user).permit( :name, 
                                  :email, 
                                  :password, 
                                  :password_confirmation)
  end

  def account_update_params
    params.require(:user).permit( :name, 
                                  :email, 
                                  :password, 
                                  :password_confirmation, 
                                  :current_password)
  end
end

```


This code overwrites the sign_up_params and account_update_params methods to accept the ```:name``` attribute. As you see, those methods are in the Devise ```RegistrationsController```, so we specified it and altered its methods. Now inside our routes we have to specify this controller, so these methods could be overwritten. Inside ```routes.rb``` change devise to:

```
devise_for :users, :controllers => {:registrations => "registrations"}
```


Open ```app/views/devise/registrations/new.html.erb``` and change form_for to:

```
<h2>Sign up</h2>
<%= bootstrap_form_for(resource, 
                       :as => resource_name, 
                       :url => registration_path(resource_name)) do |f| %>

  <%= f.text_field :name, 
             placeholder: 'username', 
             class: 'form-control' %>
  <%= f.text_field :email, 
             placeholder: 'email', 
             class: 'form-control' %>
  <%= f.password_field :password, 
                       placeholder: 'password', 
                       class: 'form-control' %>
  <%= f.password_field :password_confirmation, 
                       placeholder: 'password confirmation', 
                       class: 'form-control' %>
  <%= f.submit 'Sign up', class: 'btn sign-up-button' %>
<% end %>
```