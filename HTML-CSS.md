# HTML
- HTML is the standard markup language used to create the structure and content of a web page.
- It consists of a series of elements, each represented by a tag, and provides the basic structure of a web document.

## Box Model
- The box model is a fundamental concept in web development that describes the layout of elements on a web page.
- Every HTML element is considered a rectangular box, and the box model consists of several components that define the size and spacing of this box.
- The box model includes the following components:
1. **Content:**
   - The actual content of the box, which can include text, images, or other HTML elements.
2. **Padding:**
   - The space between the content and the inner edge of the box. Padding is used to create space around the content.
3. **Border:**
   - The border surrounding the padding. It is an optional component, and you can control its style, color, and width.
4. **Margin:**
   - The space between the border and the adjacent elements or the outer edge of the box. Margins create space between elements.
Here's a visual representation of the box model:

```
+-----------------------------------+
|              Margin               |
|  +----------------------------+   |
|  |          Border            |   |
|  |  +----------------------+  |   |
|  |  |       Padding        |  |   |
|  |  |  +----------------+  |  |   |
|  |  |  |   Content    |  |  |  |   |
|  |  |  +----------------+  |  |   |
|  |  +----------------------+  |   |
|  +----------------------------+   |
|                                   |
+-----------------------------------+
```

### Box Model Properties in CSS:
- Height, width, padding, border and margin.
   ```css
   div {
       width: 200px;
       height: 100px;
       padding: 20px;
       border: 2px solid #333;
       margin: 10px;
   }
   ```



## Inline and Block Elements

### Inline Elements:
- Elements with display property inline, only takes up as much space as it need to.
- We can't set height and width of inline elements.
- Example- `<span>`, `<a>`, `<strong>` and `<em>`, `<img>`

### Block Elements:
- Elements with display property block, blocks the entire width of the webpage.
- We can set thier height and width.
- Example- `<div>`, `<p>`, `<h1>` to `<h6>`, `<ul>`, `<ol>`, and `<li>`



## Positioning: Relative/Absolute
1. **Static Positioning-**
   - HTML default flow.
2. **Relative Positioning-**
   - An item gets position relative to it's default position.
3. **Absolute Positioning-**
   - Case 1: Item will be positioned relative to nearest positioned ancestor
   - Case 2: If no ancestor positioned, then item will be positioned relative to top-left corner of webpage.
4. **Fixed Positioning-**
   - Positioning relative to top-left corner of browser window, so when we scroll, the item doesn't moves on the screen.


# CSS
- CSS is a style sheet language used to describe the presentation of a document written in HTML.
- It defines how elements should be displayed, such as layout, colors, fonts, etc.
  
## Common CSS syling classes
1. **`.container` or `.wrapper`**
  - These classes are often used to wrap the main content of a page. They are used to set a maximum width and center the content.
2. **`.header`, `.footer`, `.sidebar`**
  - Used to style header, footer, and sidebar sections of a webpage.
3. **`.nav` or `.navbar`**
  - Applied to navigation elements or bars.
4. **`.btn` or `.button`**
  - Applied to buttons.
5. **`.form` or `.input`**
  - Applied to style forms or form inputs.



## CSS Specificity
- **The order of priority/specificity from lowest to highest is:**
1. Tag element selector:
  ```css
  tag-name{
    // CSS code
  }
  ```

2. Class selector:
  ```css
  .class-name{
    // CSS code
  }
  ```

3. Attribute selector:
  ```css
  tag-name[draggable = "___"]{
    // CSS code
  }
  ```

4. ID selector:
  ```css
  #id-name{
      // CSS code
  }
  ```

5. Inline styles:
- Styles defined inline have the highest specificity.
  ```html
  <p style="color: red;">This is red text.</p>
  ```


## CSS Responsive Queries
- There are four ways using which we can build responsive websites:
  1. Media Queries.
  2. CSS Grid.
  3. CSS Flexbox.
  4. External Frameworks.

 
## Flexbox and Grid 
- Flexbox and CSS Grid are two powerful layout models in CSS that allow you to create complex and responsive layouts with ease. Here's a brief overview of both:

### Flexbox:

- Flexbox, or the Flexible Box Layout, is designed for one-dimensional layouts, either in a row or a column. It's particularly useful for laying out items within a container along a single axis.
- Best suited for one-dimensional layouts (either rows or columns).
- Ideal for distributing space along a single axis.

1. **Container Properties:**

   - `display: flex;`: Defines a flex container.

   - `flex-direction: row | row-reverse | column | column-reverse;`: Sets the direction of the main axis.

   - `justify-content: flex-start | flex-end | center | space-between | space-around;`: Aligns items along the main axis.

   - `align-items: stretch | flex-start | flex-end | center | baseline;`: Aligns items along the cross axis.

   - `align-self: auto | flex-start | flex-end | center | baseline | stretch;`: Allows the default alignment to be overridden for individual flex items.

2. **Item Properties:**

   - `flex-grow: number;`: Defines the ability for a flex item to grow if necessary.

   - `flex-shrink: number;`: Defines the ability for a flex item to shrink if necessary.

   - `flex-basis: length | auto;`: Specifies the initial size of a flex item.

   - `flex: none | [flex-grow] [flex-shrink] [flex-basis];`: A shorthand property for setting the flex-grow, flex-shrink, and flex-basis properties.

### CSS Grid:

- CSS Grid Layout is a two-dimensional layout system that allows you to create grid-based layouts with both rows and columns.
- Best suited for two-dimensional layouts (rows and columns).
- Ideal for creating grid-based structures where items need to be placed in both rows and columns.

1. **Container Properties:**

   - `display: grid;`: Defines a grid container.

   - `grid-template-columns`, `grid-template-rows`: Specifies the size of the columns and rows in the grid.

   - `grid-template-areas`: Defines named grid areas.

   - `grid-gap` or `grid-row-gap` and `grid-column-gap`: Specifies the size of the gaps between grid items.

2. **Item Properties:**

   - `grid-column`, `grid-row`: Determines the size and location of grid items within the grid.

   - `grid-area`: Places an item onto the grid.

   - `justify-self`, `align-self`: Aligns an item inside a grid cell along the inline (for row) or block (for column) axis.

   - `place-self`: A shorthand for align-self and justify-self.
