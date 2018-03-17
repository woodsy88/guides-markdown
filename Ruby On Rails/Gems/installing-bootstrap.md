# Installing Bootstrap 3 in Rails

Add bootstrap gem to gem file

`gem 'bootstrap-sass', '~> 3.3.6'`

ensure rails sass gem is already in your gem file and installed installed

`gem 'sass-rails', '>= 3.2'`

then run

`bundle install`


> make sure to restart server after installing any gems for them to take effect.


Go to assets to open the **application.css** file

Change **application.css** to **application.scss**

remove the 2 lines from the **application.scss**

```
*= require_self
*= require_tree .
```

Add these 2 lines of code to the now empty scss file

```
@import "bootstrap-sprockets";
@import "bootstrap";
```



Add Bootstrap jQuery  to gem file

```gem 'jquery-rails'```

then run

```bundle```

Last step is to require Bootstrap and jQuery in the application’s JavaScript file. Go to **application.js** and add:

```
//= require jquery
//= require bootstrap-sprockets
```

> add require jquery at the very top and require bootstrap-sprockets at the very bottom, below require tree
___




## Installing Bootstrap 4 in Rails

git repo for installing bootstrap 4

https://github.com/woodsy88/book-app/pull/1/files

## intsall bootsrap views for devise and entire app

https://www.udemy.com/the-complete-ruby-on-rails-developer-course/learn/v4/t/lecture/3852900?start=0
