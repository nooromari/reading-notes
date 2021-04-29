## Objects

| objects | containers for named values called properties or methods. |
| property | a variable is part of an object. |
| method | a function is part of an object. |


**Object Definition:**

*Example:*

`var person = {`
  `firstName: "Noor",`
  `lastName : "Omari",`
  `fullName : function() {`
    `return this.firstName + " " + this.lastName;`
  `}`
`};`


- In a function definition, `this` refers to the "owner" of the function.

- In the example above, `this.firstName` means the firstName property of this object.


**Accessing Object Properties**

You can access object properties in two ways:

1. `objectName.propertyName`

2. `objectName["propertyName"]`


**Accessing Object Methods**

You access an object method with the following syntax:

`objectName.methodName()`

*For Accessing Example above*

`name = person.fullName();`

If you access a method without the () parentheses, it will return the function definition.



## DOCUMENT OBJECT MODEL (DOM)


- The browser represents the page using a DOM tree.

- DOM trees have four types of nodes: 

 1. Document nodes. 
 1. Element nodes.
 1. Attribute nodes.
 1. Text nodes.

![DOM nodes](https://i.morioh.com/200725/6b050937.webp)


- You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax.

- Whenever a DOM query can return more than one node, it will always return a NadeList.

- From an element node, you can access and update its content using properties such as `textContent` and `innerHTML` or using DOM manipulation techniques.

- An element node can contain multiple text nodes and child elements that are siblings of each other.

- In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).

- Browsers offer tools for viewing the DOM tree.


## Problem domains

- Programming is easy if you understand the problem domain.
- If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

  1. Make the problem domain easier: cutting out cases and narrowing your focus to a particular part of the problem.
  
  2. Get better at understanding the problem domain: make sure you understand a problem inside and out before you try and solve it with code.