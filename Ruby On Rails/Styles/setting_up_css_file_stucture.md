## How to set up your base SCSS File Structure

**Base directory**

This is where I keep Sass variables and styles which are used throughout the whole app. For instance default font sizes and default elements’ styles.

```variables.scss``` to hold color variables

```default.scss``` for site wide general styles

**Partials**

Most of my styles go there. I keep all styles for separate components and pages in this directory.

``navigation.scss``

```signup.scss```

**Responsive**

```mobile.scss```

```desktop.scss```

Here I define different style rules for different screen sizes. For example, styles for a desktop screen, tablet screen, phone screen, etc.


### Import newly created files to the main application.scssfile


``` scss

// Bootstrap 
@import "bootstrap-sprockets";
@import "bootstrap";

// Variables 
@import "base/variables";

// Default styles
@import "base/default";

// Partials - main css file 
@import "partials/*";
@import "partials/layout/*";

// Media queries for a responsive design
@import "responsive/*";;

```


 > Import variables.scss file at the top to make sure that the variables are defined before we use them

 > In your CSS, put less specific selectors above and more specific selectors below. So for instance Type selectors go above Class selectors and Class selectors go above ID selectors