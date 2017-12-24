## Installing Bootstrap 3 in Rails

Add bootstrap gem to gem file

`gem 'bootstrap-sass', '~> 3.3.6'`

ensure rails sass gem is installed

`gem 'sass-rails', '>= 3.2'`

then run

`bundle install`


> make sure to restart server after installing any gems for them to take effect.


Go to assets to open the **application.css** file and add

```
@import "bootstrap-sprockets";
@import "bootstrap";
```

Change **application.css** to **application.scss**

remove the 2 lines from the **application.scss**

```
*= require_self
*= require_tree .
```

Add Bootstrap jQuery  to gem fule

```gem 'jquery-rails'```

then run

```bundle```

Last step is to require Bootstrap and jQuery in the application’s JavaScript file. Go to **application.js** and add:

```
//= require jquery
//= require bootstrap-sprockets
```

> put require jquery at the very top and require bootstrap-sprockets at the very bottom, below require tree
___




## Installing Bootstrap 4 in Rails

books 