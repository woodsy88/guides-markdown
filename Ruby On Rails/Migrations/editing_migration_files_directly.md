## Adding Columns Directly to the file

Add a column named title of type string

```t.string :title```

Add a column named content of type text

```t.text :content```

-----

## Creating associations in migration files

```t.belongs_to :category, index: true```

```t.belongs_to :user, index: true```
