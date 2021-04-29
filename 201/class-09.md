## Forms

- Whenever you want to collect information from visitors you will need a form, which lives inside a `<form>` element.
The `<form>` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons.

- This element should always carry the **action attribute** (Its value is the URL for the page on the server that will receive the information in the form when it is submitted) and will usually have a **method** (Forms can be sent using one of two methods: get or post) and id attribute too.


*Example:*

`<form action="http://www.example.com/subscribe.php"method="get">`
`<input type="password" name="password"/>`
`</form>`


![](https://cdn.wallstreetmojo.com/wp-content/uploads/2019/08/Form-Controls-in-Excel-Example-1.1.png)



- Information from a form is sent in name/value pairs. Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server. So, You should never change the name of a form control in a page unless you know that the code on the server will understand this new value.

- HTML5 introduces new form elements which make it easier for visitors to fill in forms. Such as **form validation** which is forms on the web that give users messages if the form control has not been filled in correctly.



## CSS:Lists, Tables & Forms


- List markers can be given different appearances using the `list-style-type` and `list-style-image` properties. The `list-style-position` property specifies the position of the list-item markers (bullet points).

- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

**Table Borders:**

To specify table borders in CSS, use the `border` property.

The example below specifies a black border for `<table>`, `<th>`, and `<td>` elements:

`table, th, td {border: 1px solid black;}`

![](https://lh3.googleusercontent.com/proxy/7Gs3pcQhgDg2q9oiqHLsd7W41U_E-1-W8xAWTeLJOo9DhibQqUpWtKcnD6xfKFUbEV9Owmyw0ivObhyQ3ja7k-HqXLWchHC4iar-KDgfXg)

 that the table in the examples above have double borders. This is because both the table and the `<th>` and `<td>` elements have separate borders. To remove double borders use `border-collapse` property.

![](https://lh3.googleusercontent.com/proxy/3wursr15wHTeS-jkRpSO1Eh16C5nKRuk1aXIlbYynDgyqZ6R1sPEBjXxwFGgZgumYyQFXGE6ZgU81yhiznKvoS0hdMtj-knC8Tjr)


- Forms are easier to use if the form controls are vertically aligned using CSS. The `:focus` pseudo-class is used to change the background color of the text input when it is being used, and the `:hover` psuedo-class applies the same styles when the user hovers over them.

- `transition` property to animate the width of the search input when it gets focus.


## Events

- Events are the browser's way of indicating when something has happened (such as when a page has finished loading or a button has been clicked). 

- Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.

- When an event occurs on an element, it can trigger a JavaScript function. When this function then changes the web page in some way, it feels interactive because it has responded to the user.

![](https://lh3.googleusercontent.com/proxy/OwCSnro8hXjXJtMX-qMw7JmczmXOCfb4RpkuO5qK8BaCMpPqHX5GrL_GikQAuyonKcktoCWRFJlsES-LNSdcniyDvRtONQ1t5nGsDkTDUqOVgsdrHiXX-z-IECETO66lTLmV79F5vBEy)

- You can use event delegation to monitor for events that happen on all of the children of an element.

- The most commonly used events are W3C DOM events, although there are others in the HTMLS specification as well as browser-specific events.


![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/Ways-of-Using-JavaScript-Events-1200x720.png)
