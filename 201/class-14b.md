## CSS Transitions & Animations


![](https://miro.medium.com/max/2800/1*tQLb0ZSlFghqWmbzvUcZDA.png)

- The `@keyframes` rule specifies the animation code. The animation is created by gradually changing from one set of CSS styles to another.

- During the animation, you can change the set of CSS styles many times. Specify when the style change will happen in percent, or with the keywords "from" and "to", which is the same as 0% and 100%.
  - 0% is the beginning of the animation.
  - 100% is when the animation is complete.


![](https://www.edureka.co/blog/wp-content/uploads/2019/09/Keyframe-528x297.jpg)


*Example:*

* html : 

   `<h1>4</h1>`
   `<h1>0</h1>`
   `<h1>4</h1>`

* css :

 ` body {margin:0;  font-family:sans-serif;  color:#f25252;  background:#f7f7f7; }`

`h1 { font-size:11rem;  position:absolute; transform:translate(-50%,-50%); margin:0; }`

`h1:nth-of-type(1){ animation: range 4s infinite; }`

`h1:nth-of-type(2){ left:50%; top:50%; animation: size 4s infinite; }`

`h1:nth-of-type(3){ animation: range2 4s infinite; }`

`@keyframes range {`

 ` 0%  {left:42%;top:50%;font-size:11rem;}`

 ` 25% {left:50%;top:40%;font-size:4.5rem;}`

 ` 50% {left:58%;top:50%;font-size:11rem;}`

 ` 75% {left:50%;top:60%;font-size:4.5rem;}`
 
 ` 100%{left:42%;top:50%;font-size:11rem;}`

`}`


`@keyframes range2 {`

 ` 0%  {left:58%;top:50%;font-size:11rem;}`

 ` 25% {left:50%;top:60%;font-size:4.5rem;}`

 ` 50% {left:42%;top:50%;font-size:11rem;}`

 ` 75% {left:50%;top:40%;font-size:4.5rem;}`

 ` 100%{left:58%;top:50%;font-size:11rem;}`

`}`


`@keyframes size {`

`  0%  {font-size:11rem;}`

`  25% {font-size:26rem;}`

`  50% {font-size:11rem;}`

` 75% {font-size:26rem;}`

`  100%{font-size:11rem;}`

`}`

