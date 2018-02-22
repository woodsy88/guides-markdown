standard form for

```ruby  <%= form_for @appointment, class: "form-horizontal" do |f|  %>

   <div class="form-group">
      <%= f.label :title %><br />
      <%= f.text_field :title, class: "form-control" %>
    </div>

    <div class="form-group">
      <%= f.label :appointment_time %>
      <%= f.text_field :appointment_time, class: "form-control" %>
    </div>

    <%= f.submit 'Save', class: 'btn btn-primary btn-block' %>

  <% end %>
  ```


