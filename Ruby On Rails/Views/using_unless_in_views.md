  unless the current user is type admin user, then do the block. Run block if current user admin user.

      ``` ruby
      unless current_user.try(:type) == 'AdminUser'
        flash[:alert] = "You are not authorized to access this page."
        redirect_to(root_path)
      end```

