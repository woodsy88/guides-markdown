
#Step 1
## Creating App


Go to the folder you want to create your project in

`rails new appname --database=postgresql`

Make sure to cd into the new app

run `rails s` to see the rails welcome page and ensure everything is working


Generate you first controller

```rails g controller pages```

Open a file **pages_controller.rb** and add method for the home page action

```ruby

def home
end

```

Go into your views directory, then into your pages folder and create a file named ```home.html.erb```

Open **routes.rb** and set the pages controller home action to the root page

```root to: 'pages#home'```

---

###Next set up your github repo

first, type in ```git init``` to initialize local repository

the stages your recent changes with ```git add -A```

next commit your changes locally with git commit -m "my first commit"

then head over to your github account and create a new repository

Once it is created, you will be brought to a screen where it gives you directions for add an existing app

Enter these 2 commands in your projects folder

```git remote add origin git@github.com:woodsy88/guides-markdown.git```

then finally, push your changes up to master

```git push -u origin master```


