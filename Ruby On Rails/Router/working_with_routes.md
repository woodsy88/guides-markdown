## Working With Routes

>Everytime you change the routes file, the server needs to be restarted

setting root directory

```root to: 'pages#index'```

Change the url path of a route 

```get 'login', to: 'devise/sessions#new'```

Changing mutiple devise paths

```ruby
 devise_scope :user do
    get 'login', to: 'devise/sessions#new'
    get 'signup', to: 'devise/registrations#new'
  end
```