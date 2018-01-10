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


----

## Using Resources

declare routes for index, show, new, edit, create, update and destroy actions. Then I’ve declared some custom collection routes to access pages with multiple Post instances.

```ruby
resources :posts do
  collection do
    get 'hobby'
    get 'study'
    get 'team'
  end
end
```
