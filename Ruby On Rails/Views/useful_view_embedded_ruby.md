Inspecting what an instance variable holds in the view

```<%= @post.errors.inspect %>```

Inspecting the errors that an instance variable may hold

```<%= @post.errors.inspect %>```

Adding a video tag to the view, video neeeds to be in assetpipeline

```
<%= video_tag(
    'mist.mp4',
    id: 'banner-background',
    autoplay: true,
    loop: true,
    muted: true,
    poster: 'home_bg.jpg'
) 
%>
```


Show the distance of time in words inwhich a Model instance was created - created_at column

```
Created <%= distance_of_time_in_words(comment.created_at, Time.now)   %> ago
```

When you dont want to show item.thumb_image IF item.thumb_image is empty(nil).if you dont have an thumb_image it doesnt throw an error   
    
```
<%= image_tag portfolio_item.thumb_image, 'thumb' unless portfolio_item.thumb_image.nil? %>
```

