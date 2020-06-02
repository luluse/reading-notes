#  jQuery, Events, and The DOM

## JQuery
p. 293-301
1. JQuery lets you find elements using CSS-style selectors and then do something with elements using jQuery methods.

`$('li.hot')` creates jQuery object. This function has one parameter (css-style selector)

2. Do something with the elements using jQuery methods

`$('li.hot').addClass('complete');`

- selecting elements is simpler and more accurate
- Event handeling is simpler, uses one method that works in all major browsers
- method affect all elements selecte ith having to loop through each one
- once you have made a selection, you can apply multiple methods to it

jQuery has methods that offer simpler ways to perform common tasks, like:
- loop throug elements
- add/remove elementsfrom the DOM tree
- Handle events
- Fade elements into/ out of view
- Handle Ajax requests

> Write less, do more


p. 306-331

#### Matched set/jQuery Selection

When you select one or more element , a jQuery object is returned. this is called a **Matched set** or **jQuery Selection**.

- Get information: If a jQuery selection holds more than one element, it will retrieve info from only the first element in the matched set. 

- Set information: If a jQuery selection holds more than one element, it will update all of the elements in the matched set.

- JQuery objects store references to the corresponding nodes in the DOM tree. it doesn't create copies of them. 

- Chaining: you can use more than one jQuery method on the same selection of elements using dot notation to separate them. 

`$('li').hide().delay(500).fadeIn(1400);`

- `$(document).ready()` checks than a page is ready for your code to work.

#### Getting element content

- `.html()` retrieves info from a jQuery selection, retrieves the html inside the first element, along with its descendants.

`$('li').html();` will return `<em>fresh</em> figs`

- `.text()` retrives the content from very element in the jQuery selection

`$('li').text();` will return `fresh figspine nutshoney balsamic vinegar`

#### Updating Elements

- `.html()` gives every element in the matched set the same new content, may include HTML.
- `.text()` gives every element in the matched set the same new text content. no markup.
- `.replaceWith()` replaces every element in the matched set with new content, returns the replaced elements. 
- `.remove()` removed all the elements in the matched set.

#### Inserting elements

Involves two steps:
1. create the new elements in a jQuery object
   - `var $newItem = $('<li class="new">item</li>');` 
2. use a method to insert the content into the page.
   - `.before()`
   - `.after()`
   - `.prepend()`
   - `.append()`

#### Getting and setting attributes values

- `.attr()` get or set a specified attribute and its value. `('li#one').attr('id')`
- `.removeAttr()` - `('li#one').removeAttr('id')`
- `.AddClass()`
- `.removeClass()`

#### Getting and setting CSS properties

- `varBckgroundColor = $('li').css('background-color');` will store background color of **first** li element.

- to set a css property: `$('li').css('background-color', '#272727');`

- to set multiple properties: 

`$('li').css({`

`'background-color': '#272727',`
 
`font-family: 'courier'`

`});`

#### Working with Each

recreate the functionality of a loop using `.each()` method. allows you ti perform one or more statement on each of the itemsin the selection of element that is returned by a selector.

It takes on parameter:  a function containing the statements you want to run on each element.

`this` allow you to access the current element in the selection as method goes through.

`$('li').each(function(){`

  ` var ids = this.id;`

  ` $(this).append(' <em clas="order">' + ids + '</em>');`

`});`

#### Event methods

`.on()` handle all events. takes two paramethers:
- the event you want to respond to
- the function you want to run when event occurs

`$('li').on('click', function(){`

  ` $(this).addClass('complete');`

`});`





### Where to place your sripts:

Before the closing `</body>` tag.
