### Using font awesome in views


# font awesome gem short hand - fa_icon
An icon with text beside it

```<%= fa_icon "camera-retro", text: "Take a photo" %>```

Only a icon

```<%= fa_icon "camera-retro" %>```


# link_to

Just an icon with a link to a path

```<%= link_to fa_icon('pencil-square-o'), edit_blog_path(blog) %> ```

Just an icon with a link to a path - 2

```<%= link_to "", root_path, class: 'fa fa-home' %>```

Delete icon with delete path

```<%= link_to fa_icon('trash'), blog, method: :delete, data: { confirm: 'Are you sure?' } %>```

Icon, with text, linked to outside source

```<a href="github.com"><%= fa_icon "github", text: "my github" %></a>```

Link with favicon icon

```<%= link_to ("<i class='fa fa-rocket'></i> " +'View All Guides').html_safe, guides_page_path, class: 'all-guides-link'  %>```
