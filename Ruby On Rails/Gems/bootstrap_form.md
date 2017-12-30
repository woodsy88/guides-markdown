
# Bootstrap Form


## Gem Overview
Lets you replace form_for with bootstrap_form_for, which provides easier bootstrap styling

## Installation Instructions
How to install and setup gem

## Usage
how to use the gem

**Rubygems.org Link**

[I'm an inline-style link](https://www.google.com)

**Documentation Link**

[I'm an inline-style link](https://www.google.com)

**Repositiry Links**

[I'm an inline-style link](https://www.google.com)







Navigate to and open ```app/views/devise/sessions/new.html.erb.``` replace form_for with the below bootstrap_form

```
<%= bootstrap_form_for(resource, 
                       as: resource_name, 
                       url: session_path(resource_name)) do |f| %>

    <%= f.email_field :email, 
                      autofocus: true, 
                      class: 'form-control', 
                      placeholder: 'email' %>

    <%= f.password_field  :password, 
                          autocomplete: "off", 
                          class: 'form-control',
                          placeholder: 'password' %>


  <% if devise_mapping.rememberable? -%>
     <%= f.check_box :remember_me %>
  <% end -%>

   <%= f.submit "Log in", class: 'form-control login-button' %>
<% end %>

```

> modified form to be a bootstrap form by changing the method’s name to bootstrap_form_forand adding form-controlclasses to the fields.