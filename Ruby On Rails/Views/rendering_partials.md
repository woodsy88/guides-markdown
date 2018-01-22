----

## Short cut to rendering a partial with the same name as the instance variable

If you have a Post model, Posts Controller, posts view folder all with the same name, then when you need to loop over each post in an index view, you can just render a partial with a short form call -

```<%= render @posts %>``` in the ```index.html.erb``` view

Because post objects belong to the Post class, Rails automatically tries to render the ```_post.html.erb```partial template which is located ```views/posts/_post.html.erb```

>When you use this short cut, in the partial you do not have to use an each loop to iterate over each item

The create a corresponding view partial - ```views/posts/_post.html.erb```

```html
        <h3><%= post.title %></h3>
        <p><%= post.content %></p>

```

This will render each Post item without using the .each loop


-----

## Using If Statement In Partial

You can use an if statement in a partial

```<%= render 'shared/audit_log_tab' if policy(AuditLog).index? %>```

to add logic to render the partial or not


------

## Rendering Custom Partial with Custom controller call

> This seems the best solution for when your rendering a partial, thats file name (and instance variable name) is different from the controller, view, model names.

pass local variables that corresponds to controller instance variable in the view

```<%= render partial: 'pending_approval', locals: { pending_approvals: @pending_approvals} %>```

>notice pending_approval.each is a local variable

In the corresponding partial ```_pending_approval.html.erb``` you use the pending_approval local variable, that is calling to the controller instance variable in the above render call.

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

The controller action

```
  def homepage
    @pending_approvals = Post.where(status: 'submitted')
  end
```
