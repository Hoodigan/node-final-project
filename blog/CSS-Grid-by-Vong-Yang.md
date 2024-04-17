---
title: Small Introduction to CSS Grids
author: Vong Yang
---

# CSS Grid
## What is it?
> CSS Grid is a two-dimensional layout system that allows developers to create complex grid layouts with ease. Its concept is similar to tables. It is used to divide a page into different sections and defines the size, position, and layer, allowing for a visually appealing webpage. In short, CSS Grid is a versatile tool to help structure and organize content on a web page.

## How to use it
> CSS Grid does not require any links or installation; as the name implies, it is part of CSS. To implement it, you need to define a grid container by targeting an HTML element and setting its display property to grid. The most common way to do this would be to create a class.
### HTML
```html
<div class="wrapper">
        <div class="one box">One</div>
        <div class="two box">Two</div>
        <div class="three box">Three</div>
        <div class="four box">Four</div>
        <div class="five box">Five</div>
        <div class="six box">Six</div>
        <div class="seven box">Seven</div>
</div>
```

### CSS
```CSS
.wrapper{
    display: grid;
    
}
```

> Now, all the elements within the div in the example are grid items. Next, you'll specify the grid structure by using CSS properties to define the rows and Columns  of the grid. There are different units of measurement that can be used; however, the most common units are Pixels (px), Percentages (%), Viewport Height & Width (vh)(vw), and Grid Fraction (fr). Then, specify the properties of the grid items as follows. CSS Grid is very versatile, with many options to define the grid.
Example in use:
```CSS
/* Defines Grid Layout */
.wrapper{
    display: grid;
    max-width: 940px; /* Defines how wide the Container will be */
    margin: 0 auto; /* This will place the Container in the middle of the page */
    grid-template-columns: 1fr 1fr 1fr 1fr; /* This creates 4 Columns with evenly divided space */
    /* Note that "1fr 1fr 1fr 1fr" does not produce the same out put as "2fr 2fr" and other similar cases */
    /* Another example "grid-template-columns: 50% 25% 25%; This creates three columns with the first Column taking up 50% of the grid and the second and third taking up a foruth of 
    the grid */
    grid-template-rows: 1fr 1fr 1fr 1fr; /* This creates 4 Rows with evenly divided space  */
    gap: 10px;  /* Defines the space between each div in the grid */
}

/* Styles of Div One */
.one{
    grid-column: 1 / 3; /* The span defines the amount of space, in this case, columns, it will take up two Column */
    grid-row: 1; /* This will palce it in Row One */
}

/* Styles of Div Two */
.two{
    grid-column: 4; /* This will place it in Column 4 */
    grid-row: 1 / 3; /* This is another way to define it's properties. It determines it's staring position and it's end position, how much space it'll take up */
}

/* Styles of Div Three */
.three{
    grid-column: 3; /* This will place it in Column 3 */
    grid-row: 1 / 3; /* Starts in Row 1 and ends at Row 2 */
}

/* Styles of Div Four */
.four{
    grid-column: 4; /* This will place it in Column 4 */
    grid-row: 3 / 5; /* Starts in Row 3 and ends at Row 4 */
}

/* Styles of Div Five */
.five{
    grid-column: 1 / 4; /* Starts in Column 1 and ends at Column 3 */
    /* Note: at grid position Column 3 at Row 2, the space is already taken by Box Three, therfore an overlap will be caused */
    grid-row: 2 / 3; /* Starts in Row 2 and ends at Row 2. This is an example of redudancy. This code can be replaced with a 2, since it only exists in Row 2 */
}

/* Styles of Div Six */
.six{
    grid-column: 2; /* This will place it in Column 2 */
    grid-row: 1 / 5; /* Starts in Row 2 and ends at Row 4 */
    /* Note: at grid position Column 2 at Row 1 and Row 2, the space is already taken by Box one and Box Five, therfore an overlap will be caused */
}

/* Styles of Div Seven */    
.seven{
    grid-column: 1 / 4; /* Starts in Column 1 and ends at Column 3 */
    grid-row: 3 / 5; /* Starts in Row 3 and ends at Row 4 */
    /* Note: Box Seven and Box Six will overlap */
}

/* Styling the Grid Items */
.box{
    border: 2px solid rgb(233 171 88);
    border-radius: 5px;
    background-color: rgb(233 171 88 / 50%);
    padding: 1em;
    color: #d9480f;
}

```
> The code above will produce this outcome
> ![CSS Grid Example](/public/images/css-grid-example.png)

## Resources
[MDN: Baisc Concepts](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout)

[MDN: Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)

[W3Schools](https://www.w3schools.com/css/css_grid.asp)