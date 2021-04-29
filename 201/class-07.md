## Domain Modeling

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

**Here's some tips to follow when building your own domain models:**

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.


## Tables

- The `<table>` element is used to add tables to a web page.
- A table is drawn out row by row. Each row is created with the `<tr>` element.
- Inside each row there are a number of cells represented by the `<td>` element (or `<th>` for the header).

**Example:**

![html table](https://flaviocopes.com/html-tables/no-styling.png)


- You can make cells of a table span more than one row or column using the `rowspan` and `colspan` attributes. These attributes can be used on a `<th>` or `<td>` element.

   * **rowspan:** indicate how many *rows* a cell should span down the table.

   * **colspan:** indicates how many *columns* that cell should run across.

   *Example:* `<th colspan="2">Phone</th>`

- For long tables you can split the table into a `<thead>`(for the headings of the table), `<tbody>`(for the body), and `<tfoot>`(for the footer).These elements allow you to style these sections in a different manner than the rest of the table.


## FUNCTIONS, METHODS & OBJECTS

- Functions allow you to group a set of related statements together that represent a single task. Also, can take parameters (information required to do their job) and may return a value.

- An object is a series of *variables* (are known as **properties**) and *functions* (are known as **methods**) that represent something from the world around you.


### Object model

**Browser Object Model(BOM)**


![](https://hsheikhm.files.wordpress.com/2016/02/screen-shot-2016-02-14-at-17-42-48.png)



- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.


![](https://learn.javascript.ru/article/browser-environment/windowObjects.png)



- JavaScript also has several built-in objects such as String, Number, Math, and Date. Their properties and methods offer functionality that help you write scripts.


**Math object:**


![](https://slideplayer.com/slide/14088710/86/images/2/Math+Object.jpg)



**Date object:**


![](https://www.oreilly.com/library/view/jquery-and-javascript/9780133410877/graphics/02tab05.jpg)



- Arrays and objects can be used to create complex data sets (and both can contain the other).

