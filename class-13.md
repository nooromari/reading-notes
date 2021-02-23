## The Past, Present, and Future of Local Storage for Web Applications


Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

1. Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.

2. Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL).

3. Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful.


- HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.


 ![](https://i.pinimg.com/originals/f3/e5/b7/f3e5b7b637083a78b1b977be54e60364.jpg)



- HTML5 Storage it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.


- HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected JavaScript datatype.

- Calling **setItem()** with a named key that already exists will silently overwrite the previous value. Calling **getItem()** with a non-existent key will return null rather than throw an exception.

- Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. 

- There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).


`interface Storage {`
  `deleter void removeItem(in DOMString key);`
 ` void clear();`
`};`


*Calling `removeItem()` with a non-existent key will do nothing.*

- Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

`interface Storage {`
 ` readonly attribute unsigned long length;`
  `getter DOMString key(in unsigned long index);`
`};`

*If you call `key()` with an index that is not between 0–(length-1), the function will return null.*


- If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the `window` object whenever `setItem()`, `removeItem()`, or `clear()` is called and actually changes something. 


![](https://image.slidesharecdn.com/html5localstorage-140511235722-phpapp01/95/html5-local-storage-12-638.jpg?cb=1399852926)


