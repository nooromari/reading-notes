# CSS

CSS allows you to create rules that specify how the content of an element should appear. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.


![CSSselector](https://hackernoon.com/drafts/2z4a3yh4.png)

* Selectors: indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.
* Declarations: sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon.  
*You can specify several properties in one declaration, each separated by a semi-colon.*

  * Properties: indicate the aspects of the element you want to change.
  * Values: specify the settings you want to use for the chosen properties.


## Using CSS

### External:

The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It lives inside the `<head>` element. It should use three attributes:

`<link href="css/styles.css" type="text/css"rel="stylesheet" />`

1. href: This specifies the path to the CSS file (which is often placed in a folder called css or styles).
1. type: This attribute specifies the type of document being linked to. The value should be text/css.
1. rel: This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

*When building a site with more than one page, you should use an external CSS style sheet.*



### Internal:

You can also include CSS rules within an HTML page by placing them inside a `<style>` element, which usually sits inside the `<head>` element of the page.

Example:

`<style type="text/css">`
`body {`
`font-family: arial;`
`background-color: rgb(185,179,175);}`
`h1 {color: rgb(255,255,255);}`
`</style>`


## Color

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

1.	**rgb values**
These express colors in terms
of how much red, green and blue are used to make it up. For example: `rgb(100,100,90)`

1.	**hex codes**
These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: `#ee3e80`

1.	**color names**
There are 147 predefined color names that are recognized by browsers. For example: `DarkCyan`.



| Hue     | is the colloquial idea of color    | 
| Saturation | is the amount of gray in a color   | 
| Lightness  | is the amount of white (lightness) or black (darkness) in a color | 
| Values   | Put Pipes In | 


4. The **hsl** color property has been introduced in *CSS3* as an alternative way to specify colors. The value of the property starts with the letters hsl, followed by individual values inside parentheses for:

- hue: This is expressed as an angle (between 0 and 360 degrees).
- saturation: This is expressed as a percentage.
- lightness: This is expressed as a percentage with 0% being white, 50% being normal, and 100% being black.

CSS3 allows you to specify colors as hsl values, with an optional opacity value. It is known as `hsla`, while tha a is for alpha.

- alpha: fourth value which represents transparency This is expressed as a number between 0 and 1.0  .

![](https://i0.wp.com/www.cssscript.com/wp-content/uploads/2017/01/Minimal-HSLA-Color-picker-With-Pure-JavaScript.png?fit=543%2C408&ssl=1)

CSS3 Also, has introduced an extra value for `rgb` colors to indicate opacity. It is known as `rgba`. 

