## Images

The HTML `<img>` tag is used to embed an image in a web page. It is an empty tag (does not have a closing tag).

The <img> tag has two required attributes:

- src - Specifies the path to the image
- alt - Specifies an alternate text for the image

*Syntax:*
`<img src="url" alt="alternatetext">`

### Three Rules for Creating Images:

1. Save images in the right format: Websites mainly use images in *jpeg, gif, or png*.

2. Save images at the right size: You should save the image at the same width and height it will appear on the website.

3. Use the correct resolution Computer screens are made up of dots known as *pixels*. Images created for the web should be saved at a resolution of 72 ppi. The higher the resolution of the image, the larger the size of the file.

- Photographs are best saved as JPEGs; illustrations or logos that use flat colors are better saved as GIFs.


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




The **hsl** color property has been introduced in *CSS3* as an alternative way to specify colors. The value of the property starts with the letters hsl, followed by individual values inside parentheses for:

- *hue* : This is expressed as an angle (between 0 and 360 degrees).
- *saturation* : This is expressed as a percentage.
- *lightness* : This is expressed as a percentage with 0% being white, 50% being normal, and 100% being black.

CSS3 allows you to specify colors as hsl values, with an optional opacity value. It is known as `hsla`, while tha a is for alpha.

- alpha: fourth value which represents transparency This is expressed as a number between 0 and 1.0  .


![](https://i0.wp.com/www.cssscript.com/wp-content/uploads/2017/01/Minimal-HSLA-Color-picker-With-Pure-JavaScript.png?fit=543%2C408&ssl=1)


CSS3 Also, has introduced an extra value for `rgb` colors to indicate opacity. It is known as `rgba`. 



## Text

- There are properties to control the choice of font, size, weight, style, and spacing.

  *Example:*
   `font-style: italic;`  
   `font-weight: bold;`

- There is a limited choice of fonts that you can assume most people will have installed because that a browser will usually only display it if it's installed on that user's computer.

- If you want to use a wider range of typefaces there are several options, but you need to have the right license to use them.

- You can control the space between lines of text (`line-height: 1.4em;`), individual letters (`letter-spacing: 0.2em;`), and words (`word-spacing: 1em;`). 

- Text can also be **aligned** to the left, right, center, or justified (This indicates that every line in a paragraph,except the last line, should be set to take up the full width of the containing box.). It can also be **indented**.

  *Example:*
   `text-align: left;`
   `text-indent: 20px;`

- You can use pseudo-classes to change the style of an element when a user hovers `:hover` over or clicks on text, or when they have visited `:visited` a link.


![](https://i1.wp.com/www.tutorialbrain.com/wp-content/uploads/2019/03/CSS-Font-Property_tutorialbrain.png?fit=800%2C800&ssl=1)
