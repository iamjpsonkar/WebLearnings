> # HTML : Hyper Text Markup Language

## Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
</head>
<body>
  Content
</body>
</html>
```

## Headings

<h1>H1 Heading</h1>
<h2>H2 Heading</h2>
<h3>H3 Heading</h3>
<h4>H4 Heading</h4>
<h5>H5 Heading</h5>
<h6>H6 Heading</h6>

## Paragraph

<p>P Paragraph</p>

## List

### Ordered List
<ol>
  <li> OL > LI > 1. </li>
  <li> OL > LI > 2. </li>
</ol>

### Unordered List
<ul>
  <li> UL > LI > ● </li>
  <li> UL > LI > ● </li>
</ul>

## Span
<span>This is a SPAN</span>

## NAV
<nav>This is a NAV</nav>

## Header
<header> This is an HEADER</header>

## Article
<article> This is an ARTICLE</article>

## Div
<div>This is a DIV</div>

## Image
<img src="#" alt="This is an IMAGE" />

## LINK
<a href="#"> This is an A</a>

> # CSS : Cascading Style Sheet

## CSS Rule Structure
```
CSS Rule -->
selector {
  Property : Value; <-- Declaration/style
}
```
```css
h1{
  color : blue;
  text-align : center;
  font-size : 20px;
}
```

## Types of CSS

### Inline CSS
Rules are declared inside the Tag
```html
<h1 style="color:blue;">Blue H1 Using Inline CSS</h1>
```

### Internal CSS
Rules are declared inside the style element of the head
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
  <style>
    h1{
      color: blue;
    }
  </style>
</head>
<body>
  <h1>Blue H1 Using Internal CSS</h1>
</body>
</html>
```

### External CSS
Rules are declared in an external sylesheet_name.css and then included in an Html file using the link element
Below is the stylesheet.css
```css
h1 {
  color:blue;
}
```
Below is the index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
  <link href="./stylesheet.css" type="text/css" rel="stylesheet"/>
</head>
<body>
  <h1>Blue H1 Using External CSS</h1>
</body>
</html>
```

## Common CSS Rules

- color: set the color of the text to the specified value
  ```css
  p {
    color:blue;
  }
  ```

 - font-size: set the size of the text to the specified value
    ```css
    p {
      font-size:2opx;
    }
    ```

- font-family: set the font of the text to the specified value
  ```css
  p {
    font-family:sans-serif;
  }
  ```

- text-transform: transform the text using the specified value
  ```css
  p {
    text-transform:uppercase;
  }
  ```

- font-style: set the style of the text to the specified value
  ```css
  p {
    font-style:italic;
  }
  ```

- line-height: set the spaces between the lines of text to the specified value multiplied by the font size
  ```css
  p {
    line-height:1.5;
  }
  ```

- text-align: set the alignment of the text by the specified value inside the element
  ```css
  p {
    text-align:center;
  }
  ```

- background-color: set the background color of the text by the specified value
  ```css
  p {
    background-color:#f7f7f7;
  }
  ```

- border: set the border property of the text by the specified values
  ```css
  p {
    border:1px solid black;
    /* border: border-size border-type border-color;*/
    /* border-top, border-bottom, border-left, border-right */
  }
  ```

- text-decoration: set the decoration of the text by the specified values
  ```css
  p {
    text-decoration:underline dotted orangered;
    /* text-decoration: text-decoration-line text-decoration-style text-decoration-color*/
  }
  ```

## Combining Selectors
We can specify multiple selectors comma-separated for the common CSS rules
```css
h1, h2, h3 {
  font-family;sans-serif;
}
```

We can also specify rules for a descendent selector using space-separated elements
```css
div p {
  font-size:20px;
}
```

## CSS Selectors

### ID CSS Selector
We can specify rules for an element of Html having an id attribute using ID Selector. There can be only one ID selector inside one Element.
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
  <style>
    #head1 {
      color: blue;
    }
  </style>
</head>
<body>
  <h1 id="head1" >Blue H1 Using Internal CSS</h1>
</body>
</html>
```

### Class CSS Selector
We can specify rules for related elements of the HTML having a class attribute using the class Selector. There can be multiple space-separated Classes inside one Element.
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
  <style>
    .head2 {
      color: blue;
    }
  </style>
</head>
<body>
  <h1 class="head2" >Blue H1 Using Internal CSS</h1>
  <h2 class="head2" >Blue H1 Using Internal CSS</h2>
  <h3 class="head2" >Blue H1 Using Internal CSS</h3>
</body>
</html>
```

### Element Selector
```css
p {
  color:black;
}
```

### Important selector
```css
p {
  color:#000000 !important;
}
```

## Working with Colors

### The RGB Model
Every color can be represented using a combination of Red, Green and Blue

- RGB notation:
  Red, Green, Blue = [0, 255], [0, 255], [0, 255]
  ```css
  /* red color*/
  p{
    color:rgb(255, 0, 0);
  }
  ```

- RGBA notation: 
  We can specify an alpha/transparency value for colors using RGBA
  Red, Green, Blue, Alpha = [0, 255], [0, 255], [0, 255], [0.0, 1.0]
  ```css
  /* red color*/
  p{
    color:rgba(255, 0, 0, 0, 1);
  }
  ```

- Hexadecimal notation:
  Red, Green, Blue = [00, ff], [00, ff], [00, ff]
  ```css
  /* red color*/
  p{
    color:#ff0000;
  }
  ```

**If all the values specified for RGB are the same we get a gray color from white to black**


## Pseudo Classes

### Selector:first-child
This selects all the first children of type Selector.

```html
<style>
  li:first-child {
    font-weight:bold;
  }
</style>
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
<br/>
<ol>
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
```

Output will be
> - **One**
> - Two
> - Three
> 
> 1. **First**
> 2. Second
> 3. Third

### Selector:last-child
This selects all the last children of type Selector.

```html
<style>
  li:last-child {
    font-weight:bold;
  }
</style>
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
<br/>
<ol>
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
```

Output will be
> - One
> - Two
> - **Three**
> 
> 1. First
> 2. Second
> 3. **Third**

### Selector:nth-child(n)
This selects all the nth children of type Selector. n can be a number. n can be odd/even.

```html
<style>
  li:nth-child(2) {
    font-weight:bold;
  }
</style>
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
<br/>
<ol>
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
```

Output will be
> - One
> - **Two**
> - Three
> 
> 1. First
> 2. **Second**
> 3. Third

**In pseudo-classes, order matters, so it should be a direct child.**

### Selector: link
This will be applied to all the anchor elements having the HREF attribute.
```css
a:link{
  color:#1098ad;
  text-decoration:none;
}
```

### Selector: visited
This will be applied to all the anchor elements which are already visited.
```css
a:link{
  color: #aa2222;
}
```

### Selector: hover
This will be applied to all the anchor elements when the mouse pointer hovers them.
```css
a:hover{
  color: #aa2222;
  font-weight:bold;
  text-decoration:underline dotted #aa2222;
}
```

### a: active
This will be applied to all the anchor elements when the mouse pointer clicks them.
```css
Selector:hover{
  backgroud-color: #000000;
  font-style:italic;
}
```

## Conflicts between Selectors
When there are multiple selectors which are conflicting, then the order of priorities is as follows
1. Declaration marked (!important)
2. Inline style attribute in HTML
3. ID (#) Selector
4. Class (.) or Pseudo-class (:) Selector
5. Element (p, div, h1) Selector
6. Universal (*) Selector

**If conflicting rules are Internal and External then Preference will be given to the last saved one.**

**If conflicting rules are having the same hierarchy then Preference will be given to the last one.**

## Inheritance and the Universal Selector
CSS text properties are inherited from the parent to all the child elements. 


### Universal Selector
It is used to apply the CSS rule to everything.
```css
* {
  color:black;
}
```

## CSS Box Model
It is a rectangular box that has the following things

1. Content: Text, Images
2. Border: A outline around the Content
3. Padding: space between the content and the border
4. Margin: Outer space around the Border

Final width = left border + left padding + element width + right padding + right border

Final height = top border + top padding + element height + bottom padding + bottom border

## Margins and Paddings

### Padding
```css
div {
  padding: 10px;
  /* padding:top=10 right=10 bottom=10 left=10; */

  padding: 10px 20px;
  /* padding:top=10 right=20 bottom=10 left=20; */

  padding: 10px 20px 30px 40px;
  /* padding:top=10 right=20 bottom=30 left=40; */

  padding-top:10px;

  padding-left:10px;

  padding-right:10px;

  padding-bottom:10px;

}
```

### Margin
```css
div {
  margin: 10px;
  /* margin:top=10 right=10 bottom=10 left=10; */

  margin: 10px 20px;
  /* margin:top=10 right=20 bottom=10 left=20; */

  margin: 10px 20px 30px 40px;
  /* margin:top=10 right=20 bottom=30 left=40; */

  margin-top:10px;

  margin-left:10px;

  margin-right:10px;

  margin-bottom:10px;

}
```

**Collapsing margin, In the case of two adjacent elements, only a margin having a higher value is visible.**

## Adding Dimensions
```css
div{
  height:20px;
  width:20px;

  height:100%;
  width:50%;

  height:20px;
  width:auto;

  width:20px;
  height:auto;
}
```

## Centering

Trick to center
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Title</title>
  <style>
    .container{
      width:700px;
      margin-left:auto;
      margin-right:auto;
    }
  </style>
</head>
<body>
  
  <div class="container" style="border:1px solid black;">
    <p style="border:1px solid red;">A certified authorization professional (CAP) is a vendor-neutral certification that tests, validates and certifies an individual’s ability to understand, implement and maintain secure authorization for information systems.</p>
  </div>
</body>
</html>
```

## Types of CSS Box

### Block Level Box
1. Elements are formatted visually as a block.
2. Elements occupy 100% of the width of the parent, no matter what content they have.
3. Elements are stacked vertically by default, one after another.
4. They have line breaks after them.

Examples
```html
<body></body>
<header></header>
<main></main>
<footer></footer>
<section></section>
<nav></nav>
<aside></aside>
<div></div>
<h1></h1>
.
.
.
<h6></h6>
<p></p>
<ul></ul>
<ol></ol>
<li></li>
```
with CSS
```css
class{
  display:block;
}
```

### Inline CSS Box
1. Occupy only the space necessary for its content.
2. causes no line breaks.
3. heights and widths do not apply.
4. padding and margin are applied only horizontally.


Examples
```html
<a href="#"></a>
<img src="" alt=""/>
<strong></strong>
<em></em>
<button></button>
```
with CSS
```css
class{
  display:inline;
}
```

### Inline Block CSS Box
Combination of Inline and Block

1. Block from the inside, inline from outside
2. Occupy only content space
3. Causes no line breaks


Examples with CSS
```css
class{
  display:inline-block;
}
```

## Positioning

### Normal Flow
1. Default positioning
2. Elements "in the flow"
3. Elements are simply laid out according to their order in HTML code
```css
name{
  position:relative;
}
```

### Absolute Positioning
1. Elements are removed from the normal flow: "out of flow"
2. No impact on surrounding elements might overlap them.
3. We use the top, bottom, left or right to offset the element from its relatively positioned container.

**make parent relative, for absolute positioning**

```css
name{
  position:absolute;
  top: 0;
  bottom : 0;
  right: 0;
  left: 0;
}
```

## Pseudo Elements

### first-letter
```css
h1::first-letter{
  font-style:normal;
}
```

### first-line
```css
h1::first-line{
  font-style:normal;
}
```

### after
```css
h1::after{
  content="";
  ...;
}
```

### before
```css
h1::before{
  content="";
  ...;
}
```


# Layouts
how the text, image and other content is placed over a webpage.

## Types of layout
Arranging the different elements in an organized manner.

### Page Layout
Arranging the different components of the page.

### Component Layout
Arranging the different elements of the components.

## Way of building layout

### Using Float
The old way of building layouts of all sizes uses the float CSS property. Still used, but getting outdated fast.

-Elements are removed from the normal flow: "out of flow"

- Text and inline elements will wrap around the floated elements.

- The container will not adjust its height to the element. This is known as **collapsing of heights**.

- The container will not adjust its width to the element, and so it will put all the elements down if they are taking higher dimensions than the available ones.

```css
Selector {
  float: left; /*will take element out from normaal flow and put them in left of the flow. */
  float: right; /*will take element out from normaal flow and put them in right of the flow. */
}
```

#### Clearing floats
To avoid the problem of collapsing height we can use one trick.

1. Add an empty div with clear property

    Add an empty div inside the container, and in the style of that empty container add the clear property of CSS.
    ```css
    selector {
      clear: left; /* for left float*/
      clear: right; /* for right float*/
      clear: both; /* for both*/
    }
    ```

2. Using pseudo-element **after**
    Instead of adding an empty div to solve the problem of collapsing height, we can add a "clearfix" class in the container and add the following properties
    ```css
    .clearfix::after {
      content:"";
      clear:both;
      display:block;
    }
    ```

#### Higher width issue
This problem arises because of the box model, as the margin and the padding get added for the dimension of the element, we can use the property box-sizing to solve this issue. This will adjust the margin and padding, and hence overall dimension will be the same as the content.
```css
selector{
  box-sizing: border-box;
}
```

### Using Flexbox
The modern way of laying out elements in a 1-dimensional row without using floats. Perfect for component layouts.

Any container element, having some child can be used for flexbox. In this, the display property of the container is set to flex. This causes the elements to get horizontally aligned inside the container. All children will occupy only the required size.

```css
.container {
  display: flex;
}
```
1. Flexbox is a set of related CSS properties for building 1-dimensional layouts.
2. The main idea behind flexbox is that space inside a container element can be automatically divided by its child elements.
3. Flexbox makes it easy to automatically align items to one another inside a parent container, both horizontally and vertically.
4. flexbox solves common problems such as vertical centering and creating equal-height columns.
5. Flexbox is perfect for replacing floats, allowing us to write fewer and cleaner HTML and CSS code.

Container Element -> Flex container
Child Elements -> Flex items
Horizontal axis -> Main axis
Vertical axis -> Cross axis

#### CSS properties for Flex Container

1. **gap:0 | < length >**: To create space between items, without using a margin.
2. **justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly**: align items along the main axis (horizontally, by default)
3. **align-items: stretch | flex-start | flex-end | center | baseline**: To align items along the cross axis (vertically, by default)
4. **flex-direction: row | row-reverse | column | column-reverse**: To define which is the main axis
5. **flex-wrap:nowrap | wrap | wrap-reverse**: To allow items to wrap into a new line if they are too large
6. **align-content: stretch | flex-start | flex-end | center | space-between | space-around**: only applies when there are multiple lines (flex-wrap: wrap)

#### CSS properties for Flex Items

1. **align-self: auto | stretch | flex-start | flex-end | baseline** : To overwrite align-items for individual flex items
2. **flex-grow: 0 | < integer >**: To allow an element to growing (0 means No, 1+ means Yes)
3. **flex-shrink: 0 | < integer >**: To allow an element to shrink (0 means no, 1+ means yes)
4. **flex-basis: auto | < length >**: To define an item's width, instead of the width property
5. **flex: 0 1 auto | < int > < int > < length >** : Recommended shorthand for flex-grow, flex-shrink, flex-basis
6. **order : 0 | < integer >**: 
  Controls order of items, -1 makes item first, 1 makes it last




### Using CSS-grid
For laying out elements in a full-fledged 2-dimensional grid. Perfect for page layouts and complex components.

```css
.container {
  display:grid;
  grid-template-columns:1px 2px 3px ;
  grid-template-rows:1px 2px 3px ;
  grid-gap:1px;
  column-gap:1px;
  row-gap;1px;
}
```

- CSS Grid is a set of CSS properties for building 2-dimensional layouts
- The main idea behind the CSS grid is that we divide a container element into rows and columns that can be filled with its child elements.
- In two-dimensional contexts, CSS grid allows us to write less nested HTML and easier-to-read CSS
- CSS Grid is not meant to replace flexbox! instead, they work perfectly together.

1-D layout -> Use flexbox
2-D layout -> Use CSS grid

display: grid;
container: Grid Container;
element: Grid items;
Horizontal axis: Row Axis;
Vertical axis: Column Axis
Grid lines: separating cells of grids
Grid cell: one cell
Grid track/row: a horizontal row of grid
Grid track/columns: vertical column of grids
Gutters: space between cells (gaps)

#### Grid Containers properties
1. grid-template-rows: < track size > *
2. grid-template-columns: < track size > *
3. row-gap: 0 | < length >
4. column-gap: 0 | < length >
5. justify-items: stretch | start | center | end: **align-items inside rows (horizontally)**
6. align-items: stretch | start | center | end: **align-items inside columns (vertically)**
7. justify-content: stretch | start | center | end: **align the entire grid inside the grid container (horizontally) if the container is larger than the grid.**
6. align-content: stretch | start | center | end: **align the entire grid inside the grid container (vertically) if the container is larger than the grid.**

#### Grid Items properties
1. grid-column: < start line > / < end line > | span < number >: **To place a grid item into a specific cell, based on line numbers. span keyword can be used to span an item across more cells.**
2. grid-row: < start line > / < end line > | span < number >: **To place a grid item into a specific cell, based on line numbers. span keyword can be used to span an item across more cells.**
3. justify-self: stretch | start | center | end : **To overwrite justify-items for single item;**
4. align-self: stretch | start | center | end : **To overwrite align-items for single items;**

In **grid-template-rows** and **grid-template-columns** instead of using **Npx**, you can use **Xfr**, where X means Xth fraction of the total size. If you put **auto** then it will automatically adjust according to the remaining space.

#### repeat function of CSS
```css
.container {
  display:grid;
  grid-template-columns: repeat(4, 1fr); /* This will create grid-template-columns: 1fr 1fr 1fr 1fr; */
}
```

#### using grid-column and grid-row
```css
.element--4{
  grid-column: 2 / 3; /* This will move to the grid item to 2nd column */
  grid-row: 1 / 2; /* This will move to the grid item to 1st row */
}

.element--4{
  grid-column: 2; /* This will move to the grid item to 2nd column */
  grid-row: 1; /* This will move to the grid item to 1st row */
}

.element--4{
  grid-column: 2 / 5; /* This will move to the grid item from 2nd column to 5th column*/
  grid-row: 1 / 3; /* This will move to the grid item from 1st row to 4rd row*/
}

.element--4{
  grid-column: 2 / span 3; /* This will move to the grid item from 2nd column 2nd + 3 column*/
  grid-row: 1 / span 3; /* This will move to the grid item from 1st row to 1st + 3 row*/
}

.element--4{
  grid-column: 1 / -1; /* This will cover the whole column*/
  grid-row: 1 / -1; /* This will cover the whole row*/
}
```