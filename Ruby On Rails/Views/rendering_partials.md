----

## Short cut to rendering a partial with the same name as the instance variable

you can use

```<%= render @posts %>``` in the view

Because post objects belong to the Post class, Rails automatically tries to render the ```_post.html.erb``` partial template which is located ```views/posts/_post.html.erb```

>When you use this short cut, in the partial you do not have to use an each loop to iterate over each item

in the ```views/posts/_post.html.erb```

```html
        <h3><%= post.title %></h3>
        <p><%= post.content %></p>

```

This will render each Post item


-----


You can use an if statement in a partial

```<%= render 'shared/audit_log_tab' if policy(AuditLog).index? %>```

to add logic to render the partial or not


------

## Rendering Custom Partial with Custom controller call

Have to use render partial when your passing local variables to it

```<%= render partial: 'pending_approval', locals: { pending_approvals: @pending_approvals} %>```

corresponding partial is ```_pending_approval.html.erb```

>notice pending_approval.each is a local variable

> This seems the best solution for when your rendering a partial, thats file name (and instance variable name) is different from the controller, view, model names.

```
<% pending_approvals.each do |pending_approval|  %>
    <div class='homepage-block col-md-3'>
        <h4><%= pending_approval.user.full_name %></h4>
        <p>
            <span class="pending-details">Date submitted:</span>
            <%= pending_approval.date %>
        </p>
        <p>
            <span class="pending-details">Rationale</span>
            <%= truncate pending_approval.rationale, length: 42 %>
        </p>
    </div>
<% end %>
```

controller action

```
  def homepage
    @pending_approvals = Post.where(status: 'submitted')
  end
```
