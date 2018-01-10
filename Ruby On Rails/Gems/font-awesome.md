## Installing Font Awesome Gem

Add font awesome to gem file

```gem 'font-awesome-rails'```

Then import font awesome in application.scss

```@import "font-awesome";```

### Using font awesome in views

An icon with text beside it

```<%= fa_icon "camera-retro", text: "Take a photo" %>```

Only a icon

```<%= fa_icon "camera-retro" %>```

Just an icon with a link to a path

```<%= link_to fa_icon('pencil-square-o'), edit_blog_path(blog) %> ```

Delete icon with delete path

```<%= link_to fa_icon('trash'), blog, method: :delete, data: { confirm: 'Are you sure?' } %>```

Icon, with text, linked to outside source

```<a href="github.com"><%= fa_icon "github", text: "my github" %></a>```

Adding a custom class to the icons to change their colors

```<%= link_to fa_icon('trash'), post_path(post), id: "delete_#{post.id}_from_index", class: 'index-icons', method: :delete, data: { confirm: "Are you sure?" }  %>```

```<%= link_to fa_icon('pencil-square-o'), edit_post_path(post), class: 'index-icons', id: "edit_#{post.id}" if policy(post).update? %>```

