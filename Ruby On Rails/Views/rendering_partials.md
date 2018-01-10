----

## Short cut to rendering a partial with the same name as the instance variable

you can use

```<%= render @posts %>```

Because post objects belong to the Post class, Rails automatically tries to render the ```_post.html.erb``` partial template which is located ```views/posts/_post.html.erb```

>When you use this short cut, in the partial you do not have to use an each loop to iterate over each item

in the ```views/posts/_post.html.erb```

```html
<div class="col-sm-3 single-post-card" id=<%= post_path(post.id) %>>
  <div class="card">
    <div class="card-block">
      <h4 class="post-text">
        <%= truncate(post.title, :length => 60) %>
      </h4>
      <div class="post-content">
        <div class="posted-by">Posted by <%= post.user.name %></div>
        <h3><%= post.title %></h3>
        <p><%= post.content %></p>
        <%= link_to "I'm interested", post_path(post.id), class: 'interested' %>
      </div>
    </div>
  </div><!-- card -->
</div><!-- col-sm-3 -->
```

This will render each Post item

-----


