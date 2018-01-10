# Factory Girl
factory_girl gem gives us ability to add sample data very easily, whenever we need it.

Factory girl allows you to define test data for objects in one spot, and then use it in your test files.

If for example you ever need to change a User and add a new column, then you can do it in one spot and it takes effect throughout all your tests.


## Installation Instructions

Add the gem  ```gem 'factory_girl_rails'``` to the ```test group``` in the gem file.

Run ```bundle install```

> Factory girl gem as been deprecated and it now uses ```factory_bot```

## Usage

Make sure you have rspec installed and an ```spec``` directory

Create a new folder called ```factories```

Inside the factories folder create a new file for each object you want to create sample data for.

We will use ```specs/factories/users.rb``` as an example

**The Sequence method**

the sequence method.every additional User record, n value gets incremented by one. I.e. the first created user‘s name is going to be test0, the second one’s test1, etc.

```ruby
FactoryGirl.define do
  factory :user do
    sequence(:name) { |n| "test#{n}" }
    sequence(:email) { |n| "test#{n}@test.com" }
    password '123456'
    password_confirmation '123456'
  end
end
```

**Rubygems.org Link**

[factory_girl_rails](https://rubygems.org/gems/factory_girl_rails)

[factory_bot](https://rubygems.org/gems/factory_bot)

**Updating to factory bot guide**

[upgrading to factory_bot](https://github.com/thoughtbot/factory_bot/blob/v4.9.0/UPGRADE_FROM_FACTORY_GIRL.md)

**Documentation Link**

[Factory Girl Documentation](http://www.rubydoc.info/gems/factory_girl/file/GETTING_STARTED.md)

**Repositiry Links**

[Installed factory girl, set up factories for users and posts](https://github.com/woodsy88/overtime-app-main/commit/b58535998d02917499dff690d1abb9905ce7ad4f)

[Created model test data with factory girl](https://github.com/woodsy88/overtime-app-main/commit/e7646447d39f1108b404e10e7079d423122bad8c)

http://www.rubydoc.info/gems/factory_girl/file/GETTING_STARTED.md
