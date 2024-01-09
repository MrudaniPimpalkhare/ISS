# Lecture Notes

## Markup languages
1. ASCII for text
2. Unicode text
3. Storing information beyond characters: Markup languages
- Font, style, color, systematic, layout
4. Using tags to represent a certain style

```html
<b>This is bold<b>
<li>This is a list item<li>
```
5. Examples of markup languages:
	1. LaTeX
	2. HTML
	3. XML : eXtensible Markup Language
	4. docX: Microsoft XML document format
	5. Markdown


## Accessing a webpage

1. On the client side we have a browser(Chrome, Edge, Safari) and the browser window.
2. When the client searches a webpage on the browser, it sends a request to the web server through http. (DNS)
3. http is the language in which information is transferred. (Hyper text transfer protocol)


## HTML

```html
<!DOCTYPE html>
<head>
	<title>My Webpage</title>
</head>
<body>
	<h1> Welcome to ABC </h1>
	<p> Text goes here</p>
</body>
</html>
```


1. Lists: `<ul>, <ol>, and <li>`
	- `<ul>` : unordered lists
	- `<ol>` : ordered lists
	- `<li>`: for each item
2. Links
`<a href = "url"> Link text </a>`

3. Images: does not have any special closing tag
`<img src="img_url">`

4. Tables
- `<table>...</table>`
- `<tr> row <tr>`
- `<td> data <td>`

5. Container : `<div> </div>` : making sections with certain properties and additional attributes (used in CSS)

6. Forms


## CSS

Cascading style sheets

#### HTML : Structure and content, CSS : Style

1. Inline CSS : Attributes are given within the particular text, content

`<p style="color:red, background:cyan">text</p>

2. Internal style : In header
```css
<style>
	.classname{
	color:red; background:cyan;
	}
</style>
<div class="classname">Contect</div>
```

3. External style:
```css
<link rel-"stylesheet" href="./colorful.css">`
```

4. CSS properties
```css
color:red;
background:blue;
font-size:100px;
text-align;
```


## Javascript

### Client side and server side scripting

```js
<script src="location"></script>

var count = 10;
var name = "IIIT";
var cols = ['Red', 'Green', 'Blue'];
for(var i=0;i<cols.length;i++)
{
	console.log(cols[i]);
}

//console is the hidden terminal in your browser

```

1. Functions
2. EventListeners
3. ActionListeners
4. 