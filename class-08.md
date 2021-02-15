## Layout

**Block-level** boxes start on a new line and act as the main building blocks of any layout(such as `<h1>` `<li>` ), while **Inline** boxes flow between surrounding text (such as `<img>` ).


### Containing Elements:

The containing or *parent* element is the outer box which contain a block-level element sits inside another block-level element. It is common to group a number of elements together inside a `<div>` (or other block-level) element.


### Controlling the Position

CSS has allow you to control the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

1. **Normal flow**: Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. This is the default behavior.

2. **Relative Positioning**: This moves an element from the position it would be in normal flow. It
does not affect the position of surrounding elements.

3. **Absolute positioning**: This positions the element in relation to its containing element. It is taken out of normal flow. Absolutely positioned elements move as users scroll up and down the page.

- To indicate where a box should be positioned, you may also need to use **box offset** properties to tell the browser how far from the top or bottom and left or right it should be placed.

- The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)

- Pages can be fixed width or liquid layouts.The **fixed width layout** will stay the same width no matter what size the browser window is, whereas the **liquid layout** will stretch to fill the screen.


![](https://helpx.adobe.com/content/dam/help/ar/indesign/using/alternate-layouts-liquid-layouts/_jcr_content/main-pars/image/adaptive_layout_workflow.png)



- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).

- Grids help create professional and flexible designs. The 960_12_col.css stylesheet contains all of the rules we need to control the grid layout.The HTML uses the class names:

  * `container_12` to act as a container for the whole page and indicate that we are using a 12 column grid.
  * `clearfix` to ensure that browsers know the height of the containing box, because it only contains floated elements.
  * `grid_12` to create a block that is twelve columns wide.
  * `grid_4` to create a block that is four columns wide.


- You can include multiple CSS files in one page.There are two ways:

1. Your HTML page can link to one style sheet and that stylesheet can use the @import rule to import other style sheets.

*Example:*

indide html file: `<link rel="stylesheet" type="text/css" href="css/styles.css" />`

insid css file : `@import url("tables.css");`

2. In the HTML you can use a separate `<link>` element for each style sheet.
