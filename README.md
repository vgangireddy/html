# HTML
HTML

HTML stands for “HyperText Markup Language”. This could sound scary but it simply means it is a language for describing web-pages using ordinary text. 
A regular HTML file is just a set of “tags” as a plain-text file but with a .html file extension instead of the .txt .

##Basic Structure.
Each HTML file need to have some essential tags in order to work properly those are:

* `<doctype>`: This allow the browser to detect the HTML version that we are currently, this is like a link to rules that                html pages had to follow to be considered good HTML.
* `<html>`: represent the root of an HTML document. All other elements must be descendants of this elements.
* `<head>`: This element provides general information (metadata) about the document, including its title and links to its             scripts and stylesheets. 
* `<title>`: This tag allow the developer to determine the title of the page, this title is going to be show as title of                the browser tab.
* `<meta>`: Elements represent any metadata information that cannot be represented by one of the other HTML meta related              elements.
* `<body>`: This element represents the content of an HTML document. There can be only one <body> element in a document.

##Example

```html
<doctype>
 <html>
  <head>
    <title>New Page</title>
  </head>
  <body>
    <!-- Comments -->
    <div>
      <p>
        Here we have a paragraph, that have an inline element <span>I am an inline element </span>
      </p>  
    </div>	
  </body>
</html>
```
##HTML Block and Inline Elements

The whole purpose of a HTML element  is to help the developer to style each element or a certain condition  of elements with some kind of style (using css), also to have a better organization about the text that we should like to be show.
HTML have two kind of elements, that are going to be differentiate because they have a different default display value (block and inline).

###Block-Level Elements

A block-level element always starts on a new line and takes up the full width available (100%), here are some examples:
```html
<div></div>
<h1></h1> to <h6></h6>
<p></p>
<form></form>
```

###Inline Elements

An inline element does not start on a new line and only takes up as much width as necessary.
```html
<span></span>
<a></a>
<img></img>
```

##Common Elements

* `<div>`: The HTML <div> is the generic container for flow content, which does not inherently represent anything. It can            be used to group elements for styling purposes.
* `<p>`:  This tag represent a paragraph of text. Paragraphs are usually represented in visual media as blocks of text              that are separated from adjacent blocks by vertical blank space and/or first-line indentation.
* `<span>`: This is a generic inline container for phrasing content, which does not inherently represent anything. It can             be used to group elements for styling purposes.
###Headers 

HTML have some elements that are know as headers elements that have some predefined style allowing the developer to show the enclosing text as headers, there are 6 different headers elements:

```html
<h1>The most Important</h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6>The least important</h6>
```

###List Tags

There are 2 kind of list:

* Ordered List:

```html
<ol>
	<li>
	  one
  </li>
	<li>
	  two
  </li>
</ol>
```
* Unordered List:

```html
<ul>
  <li>
    apple
  </li>
  <li>
    orange
  </li>
</ul>
```

As we can see the both of the have the same inner element `<li>` that is know was the list tag, this element is going to tell the browser that the inner text is going to be part of the ordered or unordered list, depending which one we like to use.

##Attributes.

All the HTML elements can have attributes, that is going to provide additional information about a certain element, attributes are always specified in the start tag. Attributes usually come in name/value pairs like: `<div id=”main”></div>` `id` and `class`.

`id` and `class` are attributes that could be placed inside any element, and the purpose of this attributes to allow the developer to differentiate them in order to give them a certain style (using CSS) or behavior (using Javascript) in a future.

The main difference between the id and the class attribute is that we could not repeat any id within our html document or project, because this will throw us an error and with class we can have more than one element with the same class, this because we would like to have a group of element that are going to be style together.

###Example that will thrown an error:

```html
<div id=”main”>
	<p>Hello World</p>
</div>
<div id=”main”>
	<p>
		Another Main Content
	</p>
</div>
```
###Correct Example:
```html
<div id=”main”>
		<h1>First One</h1>
  <p class=”important”>
	  Hello world
  </p>	
  <p>
	  Bye World
  </p>
</div>
<div>
	<p class=”important”>
		This is another important content
  </p>
</div>
```
##`<a>` Anchors(Link)

`<a>` tag, is known as the anchor tag that allow the developer to create a link within the actual html document or another html document, in order to do that the developer use the attribute href assigning as value the link to where the user should redirect to.

###Examples:
* Snippet 1(within a document)
```html
  <div id=”main”></div> 
  <a href=”#main”>first link</a>
```

		This snippet is going to scroll up the window until the main div is fully show.

* Snippet 2 (to another document within the same folder)
```html
  <a href=”main.html”>first link</a>  
  <a href=”about.html”>first link</a>
```
		This snippet is going to redirect to another html document within that folder.
		
* Snippet 3 (to another url)
```html
  <a href=”www.google.com”>Google</a>
```
		This snippet is going to redirect to another html document within that folder.
	
##`<img>` Image Tag	
This tag allow the user to add an image to the html document, in order to do that we are going to use the src attribute, giving the actual path of the image as value. It could have some others attributes as the alt, that receive as value a string that will be rendered if the browser could not render the image, this is very useful for screen reader hardware. The other 2 common attributes are width and height.

It is very important to remember that <img> is a self enclosing tag.

###Examples:
```html
<img src=”http://static.batanga.com/sites/default/files/styles/full/public/universo-observable-en-una-imagen-3.png?itok=sBpiT7gx” alt=”Image about universe ”width=”50%” height=”50%”> 
```
##Input

  The tag is a dynamic element that will allow interaction with the user for example if we want to create a textbox we should need to use this tag along with the type attribute with “text” as value.

###Example
```html
<input type=”text”/>
```

What happen if we don’t want a text box?, There a lot of type values that we can choose to get some information about the user.
* button:  Defines a clickable button (mostly used with a JavaScript to activate a script)
* checkbox: Defines a checkbox
* color: Defines a color picker
* date: Defines a date control (year, month and day (no time))
* datetime: The input type datetime has been removed from the HTML standard. Use datetime-local instead.
* email: Defines a field for an e-mail address
* file: Defines a file-select field and a "Browse..." button (for file uploads)
* number: Defines a field for entering a number
* password: Defines a password field (characters are masked)
* radio: Defines a radio button
* range: Defines a control for entering a number whose exact value is not important (like a slider control)
* reset: Defines a reset button (resets all form values to default values)
* search: Defines a text field for entering a search string
* submit: Defines a submit button
* text: Default. Defines a single-line text field (default width is 20 characters)
* time: Defines a control for entering a time (no time zone)
* url: Defines a field for entering a URL

There are more of them on:

[Mozilla MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

###`<textarea>` 

The HTML `<textarea>` element represents a multi-line plain-text editing control.

###`<select>`

The HTML select (`<select>`) element represents a control that presents a menu of options. The options within the menu are represented by <option> elements, which can be grouped by <optgroup>elements. Options can be pre-selected for the user.

####Some useful attributes:

* multiple: This Boolean attribute indicates that multiple options can be selected in the list. If it is not specified, then only one option can be selected at a time.

####<option>

This tag allow the developer to define predefined options that the user are going to select, the purpose is to create a select o list elements.

Note: The `<option>` tag can be used without any attributes, but you usually need the value attribute, which indicates what is sent to the server.

#####Attributes

* value: text that will specify the value that is going to be send to the server
* selected: specified that an option should be pre-selected when the page load

### Example `<select>` `<option>`

```html
<label for=”fruit>Select your favorite fruit:</label>
<select name=”fruit”>
 	<option value="apple">apple</option>
  	<option value="orange">orange</option>
  	<option value="peach">peach</option>
  	<option value="banana">banana</option>
</select>
```
[More attributes and information](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)

##Form

The HTML `<form>` element represents a document section that contains interactive controls to submit information to a web server.

This tag allow the user to submit some key and values to a certain url that will be defined using the action attribute and also allow you to choose between GET or POST as method to the submitted action.

Talking a little about HTTP, The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.

Example: A client (browser) submits an HTTP request to the server; then the server returns a response to the client. The response contains status information about the request and may also contain the requested content.

###The GET method 

This method is going to request data from a specified resource using the url to send the actual requesting information

####Example:
```html
<form action=”www.google.com” method=”GET”>	
	<label for=”user”> User Id: </label></br>
	<input name=”user” type=”text” required/></br>
	<label for=”password”> Password: </label></br>
	<input name=”password” type=”password” required/>
	</br>
	<input type=”submit” value=”submit”/></br>
</form>
```

This example is going to show within the page a user form that will request for the user id and the password, then when the user click on submit he going to be redirect to the url passed as value to the action attribute, for this example the value is www.google.com, but since we are using `GET` as method, the form is going to append a query string that will start with a question mark ? followed by a series of `name=value` pairs separated using an `& symbol`. For example if we type as username peter, then as password classified, we are going to be redirect to `www.google.com?user=peter&password=classifed`, but we can see that we have a problem here, we don’t want to show our password inside the url, for that reason we have another method (POST) to send the request that is not going to append the query on the url.

####Some notes on GET request:
* GET requests can be cached
* GET requests remain in the browser history
* GET requests can be bookmarked
* GET requests should never be used when dealing with sensitive data
* GET requests have length restrictions
* GET requests should be used only to retrieve data

###The POST Method
The main difference is that the query string is going to be sent in the HTTP message body, so it is a bit more secure that the GET method. Using the same GET example.

####Example

```html
  <form action=”www.google.com” method=”POST”>	
  	<label for=”user”> User Id: </label></br>
  	<input name=”user” type=”text” required/></br>
  	<label for=”password”> Password: </label></br>
  	<input name=”password” type=”password” required/>
  	</br>
  	<input type=”submit” value=”submit”/></br>
  </form>
```

If we access some information and we click submit the url is going to be show as www.google.com, so we are not going to have a media query within the url, for that reason this is more secure, all the information is going to be sent inside the body of the request.

####Some other notes on POST request:
* POST requests are never cached
* POST requests do not remain in the browser history
* POST requests cannot be bookmarked
* POST requests have no restrictions on data length

##Tables

In order to create a table to be show on an HTML document we are going to use the `<table>` tag along the `<th>` (table header) tag, `<tr>` (table row) tag and `<td>` for table data.
```html
<table>
  <tr>
    <th>Item</th>
    <th>Color</th>	
    </tr> 
  <tr>
  	<td>Orange</td>
  	<td>Orange </td>
  </tr>
  <tr>
  	<td>Apple</td>
  	<td>Red</td>
  </tr>
</table>
```

We can go a little further and add some semantic tags, that were included on HTML5, the whole purpose of the semantic tag is to have a better organization in order to be easy to work for the future you, or for any other developer.
Some the semantic tags that are used inside the `<table>` tag are `<thead>`, `<tbody>` and `<tfoot>`, here is the same example, already with the semantic tag.

```html
<table>
	<thead>
    <tr>
      <th>Item</th>
      <th>Color</th>	
    </tr> 
  </thead>
  <tbody>
    <tr>
    	<td>Orange</td>
    	<td>Orange </td>
    </tr>
    <tr>
    	<td>Apple</td>
    	<td>Red</td>
    </tr>	
  </tbody>
</table>
```

##References

[HTML & CSS: Design and Build Web Sites](http://www.wufai.edu.tw/information_technology_center/datasheet/HTML%20and%20CSS%20design%20and%20build%20websites.pdf)



