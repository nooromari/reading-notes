# Class 02

### Structural markup:

The elements that you can use to describe both headings and paragraphs.

| Element | Example |
| ----------- | ----------- |
| Headings : `<h1>` to `<h6>`| `<h1>Heading 1</h1>` | 
| Paragraphs | `<p>This is for a paragraph.</p>` | 
| Bold | `<b>key word</b>` | 
| Italic | `<i>Australia</i>` | 
| Superscript | `<p>2<sup>2</sup> equal 4</p>` | 
| Subscript | `<p>The water chemical formula is H<sub>2</sub>O </P>` | 
| Line Breaks:to add a line break inside a paragraph | `<p>The Earth<br />gets one hundred tons heavier every day</p>`| 
| Horizontal Rules:add a horizontal rule between sections | `<h1>This is heading 1</h1><hr><h2>This is heading 2</h2>`| 


### Semantic markup:

The elements that are not affect the web pages structure, but they do add extra information to the pages.

- **Strong**:  The use of the `<strong>` element indicates that its content has strong importance(the contents is shown in bold).

- **Emphasis**: The `<em>` element indicates emphasis that subtly changes the meaning of a sentence(the contents is shown in italic).

- **Quotations**: There are two elements used for quotations:
   1. `<blockquote>` is used for longer quotes that take up an entire paragraph.
   2. `<q>` is used for shorter quotes that sit within a paragraph.

- **Citations**: `<cite>` element used to indicate where the citation is from when you are referencing a piece of work.

- **Definitions**: The `<dfn>` element is used to indicate the defining instance of a new term.

- **Changes to Content**:
   * The `<ins>` element used to show content that has been inserted into a document.
   * The `<del>` element can show text that has been deleted from it.
   * The `<s>` element indicates something that is no longer accurate (but that should not be deleted).

- **Author Details**: The `<address>` element use to contain contact details for the page author.



## CSS

CSS allows you to create rules that specify how the content of an element should appear. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.


![CSSselector](https://hackernoon.com/drafts/2z4a3yh4.png)


* **Selectors** : indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.
* **Declarations** : sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. 

  * **Properties** : indicate the aspects of the element you want to change.
  * **Values** : specify the settings you want to use for the chosen properties.

*You can specify several properties in one declaration, each separated by a semi-colon.*


### Using CSS

#### 1.External:

The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It lives inside the `<head>` element. It should use three attributes:

`<link href="css/styles.css" type="text/css"rel="stylesheet" />`


1. *href* : This specifies the path to the CSS file (which is often placed in a folder called css or styles).
1. *type* : This attribute specifies the type of document being linked to. The value should be text/css.
1. *rel* : This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

*When building a site with more than one page, you should use an external CSS style sheet.*


#### 2.Internal:

You can also include CSS rules within an HTML page by placing them inside a `<style>` element, which usually sits inside the `<head>` element of the page.

**Example**:

`<style>`
`body {`
`background-color: rgb(185,179,150);}`
`h1 {color: rgb(155,25,255);}`
`</style>`



## JavaScript

### Variables

JavaScript variables are containers for storing data values.

#### Declaring Variables:
You can declare a variable with the var keyword: `var userName;`
After the declaration, the variable has no value (technically it has the value of `undefined`). To assign a value to the variable, use the equal sign: `userName = 'Noor';`
You can also assign a value to the variable when you declare it: `var userName = 'Noor';`

#### Variables mames:
All JavaScript variables must be identified with unique names.
The general rules for constructing names for variables (unique identifiers) are:

- Names can contain letters, digits, underscores, and dollar signs but must begin with a letter `$` or `_` .
- Names are case sensitive (x and X are different variables).
- Reserved words (like for,if) cannot be used as names.

**DATA TYPES:**

![](https://www.creatingux.com/CIT230/media/images/datatypes.png)

#### Arrays:
An array is a special type of variable that stores a list of values.

*Syntax:*

`var array_name = [item1, item2, ...];`    

*Example:*

`var names = ['noor','batool','sara'];`   *array literal*

**or**

`var names = new Array ('noor','batool','sara');`   *array constructor*


### EXPRESSIONS

An expression evaluates into a single value. There are two types of expressions.

1.	**EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE** In order for a variable to be useful, it needs to be given a value. This is done using the assignment operator (the equals sign).

 `var color = 'beige';` *The value of color is now beige.*

2.	**EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE** You can perform operations on any number of individual values to determine a single value.
 For example: `var area = 3 * 2;`  *The value of area is now 6.*


#### OPERATORS

Expressions rely on things called *operators*; they allow programmers to create a single value from one or more values.
1. **ASSIGNMENT OPERATORS** Assign a value to a variable

    `color = 'beige';`   *The value of color is now beige.*

1. **ARITHMETIC OPERATORS** Perform basic math 

    `area = 3 * 2;`   *The value of area is now 6*. 

1. **STRING OPERATORS** Combine two strings 

    `greeting= 'Hi 1 + 'Mol ly';`    *The value of greeting is now Hi Molly.*

1. **COMPARISON OPERATORS** Compare two values and return true or false

    `buy = 3 > 5;`   *The value of buy is false.*

1. **LOGICAL OPERATORS** Combine expressions and return true or false

    `buy= (5 > 3) && (2 < 4);`   *The value of buy is now true.*

#### More opeartors below:


![](https://i.pinimg.com/originals/13/09/cb/1309cb725dea3e859a873607dd298d00.png)


### Comparison

Comparison operators are used in logical statements to determine equality or difference between variables or values.

**The table below explains the comparison operators:**

![](https://i.ytimg.com/vi/wFB-ywsNPwg/maxresdefault.jpg)


### logical operators

Logical operators are used to determine the logic between variables or values.

**The table below explains the logical operators:**

![](https://slideplayer.com/slide/15945194/88/images/25/Logical+Operators+%28cont.%29.jpg)


### If statement

![](https://www.bookofnetwork.com/images/javascript-images/JS_if-else-syntax_20Sep16_1823.png)


**The following flowchart for if statement:**

![if else](https://cdn.javascripttutorial.net/wp-content/uploads/2016/08/JavaScript-if-else-statment.png)