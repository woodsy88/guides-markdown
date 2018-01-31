## Kaminari
Pagination gem


## Install

add ```gem 'kaminari', '~> 1.1', '>= 1.1.1'``` to gem file

run ```bundle```


## Usage

in your ```posts/index.html.erb``` file add


```<%= paginate @posts %>```

then in the ```posts_controller.rb``` file, in the ```index``` action

```ruby
def index
  @posts = Post.page(params[:page]).per(5)
end
```


## Styling the pagination section

run

```rails generate kaminari:views bootstrap3```

which generates the rails views

https://rails.devcamp.com/ruby-gem-walkthroughs/view-template-tools/kaminari-pagination-example

https://rubygems.org/gems/kaminari

https://github.com/woodsy88/overtime-app-main/commit/b06fc1649db42145dac00f11fbd908201f5eef35


### Setting up ajax for pagination page changes

details also in devcamp guide

github repo - https://github.com/woodsy88/overtime-app-main/commit/542a3ca8c5079dd6625afe07645927289b517bb8

https://github.com/woodsy88/portfolio-aw/commit/f76b897b43040c35eb09af4e36ade02b1117b360


video - https://www.udemy.com/professional-ruby-on-rails-coding-course/learn/v4/t/lecture/5515204?start=0
