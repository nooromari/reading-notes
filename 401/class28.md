## Django Forms

 The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

- **action**: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
- **method**: The HTTP method used to send the data: post or get.
    - The `POST` method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to cross-site forgery request attacks.
    - The `GET` method should only be used for forms that don't change user data. It is recommended for when you want to be able to bookmark or share the URL.

Django's form handling uses all of the same techniques for displaying information about our models, the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page. What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.

*A process flowchart of how Django handles form requests is shown below, starting with a request for a page containing a form (shown in green).*

![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png) 


## Django Templates

- A template is a text file that defines the structure or layout of a file (such as an HTML page), it uses placeholders to represent actual content. 

- A Django application created using startapp (like the skeleton of this example) will look for templates in a subdirectory named 'templates' of your applications.

![](https://consideratecode.com/wp-content/uploads/2018/04/template_inheritance-1000x500.png)


