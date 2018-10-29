# DOCUMENT OBJECT MODEL (DOM)

## What is DOM

The Document Object Model is the browser internal representation of a web page. When browser read the your HTML code, they create structure and model if it.

## When should i use DOM

You can use dom to :

* Inspect the page structure
* Edit the CSS styling
* Attach or remove event listeners
* Edit any node in the page
* Change any node attribute
* Display data from API

## Popular window properties and method

Here is a list of popular window properties and method :

* `console` : for print anyting inside browser`s console. Useful to print error and variable value. 

* ``


## There are various method to retrieve DOM elements

**[Get DOM Elements - Code Sample](https://codepen.io/impatbyte-network/pen/OBqQNx?editors=1010)**

* `document.getElementById()` : Returns the element with specified Id.

```html
<h2 id="title">Title</h2>
```

```js
document.getElementById("title")
```

* `document.getElementsByClassName()` : Returns a collection of all elements in the document with the specified class name (NodeList object).

```html
<ul>
    <li class="list">list1</li>
    <li class="list">list2</li>
    <li class="list">list3</li>
</ul>
```

```js
document.getElementsByClassName(".list")
```


* `document.getElementsByTagName()` : Returns a collection of an elements's child elements with the specified tag name (NodeList object).

```html
<h2 >Heading 2 Example</h2>
```

```js
document.getElementsByTagName("h2")
```

* `document.querySelector()` : Returns the first element that matches a specified **CSS selector(s)** in the document.

```html
<h2 class="example">Heading 2 Example</h2>
```

```js
document.querSelector("#title")
```

* `document.querySelectorAll()` : Returns all elements in the document that matches a specified **CSS selector(s)**(NodeList object).

```html
<ul>
    <li class="list">list1</li>
    <li class="list">list2</li>
    <li class="list">list3</li>
</ul>
```

```js
list = document.querySelectorAll(".list")
```

## Handling Event With DOM

With JavaScript DOM, you can add many event handlers to one element. To do add event handlers, we need the `addEventListener()` method.

For example, we want to display "Hello World" with `alert()` when the user clicks on an element :

```html
<button id="button">click me!</button>
```
```js
const button = document.getElementById("button")

button.addEventListener("click",function(){alert("Hello World!")})
```

reffer to external named function :

```html
<button id="button">click me!</button>
```
```js
const button = document.getElementById("button")

button.addEventListener("click",handleClick)

function handleClick() { 
    alert("Hello World!") 
}
```

 A full list is available in [MDN](https://developer.mozilla.org/en-US/docs/Web/Events), but here are some of the most common event types and event names:

 * **mouse events (MouseEvent)**: mousedown, mouseup, click, dblclick, mousemove, mouseover, mousewheel, mouseout, contextmenu
* **touch events (TouchEvent)**: touchstart, touchmove, touchend, touchcancel
* **keyboard events (KeyboardEvent)**: keydown, keypress, keyup
* **form events**: focus, blur, change, submit
window events**: scroll, resize, hashchange, load, unload


**[Add Event Listener to Single Element  - Code Sample](https://codepen.io/impatbyte-network/pen/VEgpKw)**

**[Add Event Listener to Multiple Elements - Code Sample](https://codepen.io/impatbyte-network/pen/VEgpKw)**


## Change HTML Style Using DOM

You can change HTML element's style using JavaScript DOM `style` properties.

```html
<h1 id="title">Title</h1>
```

```js
document.getElementById("title").style.backgroundColor = "red"
```

[Change HTML Element`s Style Using DOM - Code Sample](https://codepen.io/impatbyte-network/pen/QZoreQ/?editors=1010)

You also can change the css of HTML element based on specific event.


 ```html
<h1 id="title">Title</h1>
```a

```js
const title = document.getElementById("title")

title.addEventListener("mouseover", changeBackgroundToRed)

function changeBackgroundToRed() {
    title.style.backgroundColor = "red"
}
```

[Change HTML Element`s Style Based on Specific Event - Code Sample](https://codepen.io/impatbyte-network/pen/MPxXjL?editors=1010#0)


## Change HTML Style Using DOM












References :

[Flaviocopes-DOM](https://flaviocopes.com/dom/)

[Kirupa-Traversing the DOM](https://www.kirupa.com/html5/traversing_the_dom.htm)

[W3schools-DOM](https://www.w3schools.com/js/js_htmldom.asp)

[khanacademy-DOM Event Types](https://www.khanacademy.org/computing/computer-programming/html-css-js/html-js-dom-events/a/dom-event-types)

