

Strong Params method

```ruby
private

def portfolio_params
    params.require(:portfolio).permit(:title, :subtitle, :body)
end
```

Find and store in an intstances objects with attribute 

```@portfolio_items = Portfolio.where(subtitle: "Ruby on Rails")```


Find an item by its id

```@portfolio_item = Portfolio.find(params[:id])```

```(params[:id])```


Find the skill with the id of 2

```@skill = Skill.find(2)```

Find and store all blogs posts

```@post = Blog.all```