# EJS Partials

- **EJS Partials** help avoid repetition of the same code on several web pages. For example, you may want the same header or footer for several web pages for that you can use EJS partials to create a single fix content on a web page.

 
 - To use include in EJS in the template you should write `<%- include('user/show'); %>`. You'll likely want to use the raw output tag (`<%-`) with your include to avoid double-escaping the HTML output. *The file should be inside views*.
 
 
![](https://res.cloudinary.com/practicaldev/image/fetch/s--NcyF1ajR--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/gk1bxrwovuxzc5gnu6g7.png)