# Bootstrap
## Learning Goals
  - I can link bootstrap into my project.
  - I can find and search the bootstrap documentation.
  - I can use the grid system to create a responsive web page.
  - I can modify a Bootstrap component.

## Resources
  - [Bootstrap Grid System](https://getbootstrap.com/docs/4.4/layout/grid/)

## What is Bootstrap?
Bootstrap was created at Twitter to help give internal tools a consistent look. It is a CSS Framework for creating responsive, mobile first Web pages. Bootstraps main goal creating informative web pages, as opposed to Web Apps. Bootstrap provides a style definition for all HTML elements. This help to give website's a uniform feel across all browsers, remember that different browsers will have different default styles.  

## Linking Bootstrap to your Project
[Bootstrap Getting Started](https://getbootstrap.com/docs/4.4/getting-started/introduction/)  
Bootstrap is primarly a CSS Framework however some components require extra JavaScript librarys to work. A list of these components can be found at the link above. For today we will just be using the CSS file.  
To add Bootstrap to our project, add this inside of the `<head>` tag.  
```<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.0/css/bootstrap.min.css" integrity="sha384-SI27wrMjH3ZZ89r4o+fGIJtnzkAnFs3E4qz9DIYioCQ5l9Rd/7UAa8DHcaL8jkWt" crossorigin="anonymous">```   
This works in the same manor that we have been using to add our local css files, only this time it is linking to a resource that is stored in the cloud.
You should see that once we add this link and refresh our page our pages style has been updated.  

## Bootstrap 12 Grid System
Bootstrap's Grid system uses rows, columns and containers to create layouts and align content. It it built using FlexBox and uses what is know as a '12 Column Grid'. It is a way of breaking down our page into sections of different widths. It also gives us the ability to change how much space a section should take and different viewsizes (ie. a different Layout for Web and for Mobile.)  
![BootstrapGrid](https://www.c-sharpcorner.com/article/bootstrap-grid-system/Images/1.png)

## Creating a Layout with Bootstrap
The outermost element on the page is going to be a Boostrap container div `<div class="container">` all of our layout will be nested inside this div. In this div we can set a row `<div class="row">` and then set columns inside that row. All of our content must be placed inside of a column div. It is important to use this order and format as thats how the Bootstrap layout works. 
```html
<div class="container">
  <div class="row">
    <div class ="col">
      <p>Hello World!<p>
    </div>
  </div>
</div>
```

Bootstrap will automatically divide your row to fit the number of columns you have. This will work for all devices and viewports.  
```html
<div class="container">
  <div class="row">
    <div class="col fill-red">
      Column 1 of 2
    </div>
    <div class="col fill-green">
      Column 2 of 2
    </div>
  </div>
  <div class="row">
    <div class="col fill-yellow">
      Column 1 of 3
    </div>
    <div class="col fill-green">
      Column 2 of 3
    </div>
    <div class="col fill-red">
      Column 3 of 3
    </div>
  </div>
</div>
```
Some times you will will want to specify exactly how much space a certain part of you page takes up. For this we can add a screen size and width to the column class.fe
The naming convention for boostrap columns is:   
`col` - "size" - "number of spaces"  
So `col-sm-6` would mean, that on a small viewport (576px - 768px) take up 6 column slots.
|Size| Prefix | Max Width | Size Range |
|---|---|---|---|
|Extra Large | `col-xl` |1140px| > 1200px|
|Large| `col-lg` |960px| > 992px|
|Medium| `col-md`|720px| > 768px |
| Small |`col-sm`|540px |> 578px|
|Extra Small | `col-xs` | none (auto) | < 578px|
All columns have a 15px 'gutter' on either side, so allow an extra 30px if making a tightly aligned design.

By default, Bootstrap will try to squeeze content to fit inside of a row. You can specify how many rows coulumns a row has to make the content wrap.
```html
<div class="container">
  <div class="row row-cols-3">
    <div class="col fill-red">Column</div>
    <div class="col fill-yellow">Column</div>
    <div class="col fill-red">Column</div>
    <div class="col fill-yellow">Column</div>
  </div>
</div>
```
## Bootstrap Forms
## Challenges
cd into the `challenge1` directory. In there you will find `layout.html`. The page has the html elements created, but they are all over the place! Using Boostrap Refactor the layout to resemble these wireframes for mobile and desktop. You will need to link to the bootstrap CDN to the file.
### Desktop
![Desktop](./docs/Desktop-Wireframe.png)
### Mobile
![Mobile](./docs/Mobile-Wireframe.png)



