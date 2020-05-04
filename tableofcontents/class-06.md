# JS Object Literals; The DOM

## Understanding The Problem Domain Is The Hardest Part Of Programming.

while coding, the real challenge is to understant the problem domaine. If you don't have a clear picture of the elements you should be coding, it will become confusing. 

> It is very difficult to solve a problem before you know the question.

There are two things yo can do to make programming easier: 

- Make the problem domain easier: Focus to a particular part of a problem, and when you fully understand it you can expand the problem domain. 
- Get better at understanding the problem domain. Sit down and talk to customers and business people that know about the problem. Make sure you understand a problem inside and out before you try and solve it with code. It will save you lot of time.


## Object Literals

Objetcs group together a set of variables and functions to create a model of something you would recognize from the real world. 

- In an object, variables become known as **properties**. They tell us about the objetc.
- In an object, functions become known as **method**. They represent taks that are associated with the object.

Properties and methods have a name (called **key**) and a value. Objetcs cannot have two keys with the same name because keys are used to access their corresponding values.

- The value of a property can be a string, number, boolean, array or another object.
- The value of a method is always a function.

#### Creating an object using litteral notation

- The object is their curly braces and their contents. 
- The object is stored in a variable
- Separate each key from their value using a colon.
- Separate each property and their method with a comma.

#### Accessing an object and dot notation

You can access the properties or methods of an object using **dot notation**.

`namOfTheObject.propertyOrMethodName`

The period is known as the **member operator**

You can alsa access the properties or methods of an object using square brackets syntax. 

`namOfTheObject['propertyOrMethodName']`

## Document Object Model DOM

The DOM is neither part of the HTML or JS. It is a separated set of rules. It isimplemented by all major browsers makers.

API application programming interface.

#### The DOM tree is a model of a web page.

As a browser load a web page, it creates a model of that page. This is called a DOM tree, and it is stored in the browser memory. it consist of four main types of nodes:

- The cocument node: represents the entire page. 
- Element nodes: the structure of an HTML page
- Attribute nodes
- Text nodes

Each node is an object with methods and properties.

#### Working with the DOM tree

Accessing and updating the DOm tree involves two steps:
- locate the node that represents the element you want to work with
- Use its text content, child elements and attributes

#### DOM Queries

methods that find elements in the DOM tree. DOM queries can return one element or a NodeList (**collection** of nodes).

methods that return a single element node:
- `getElementById();` in HTML
- `querySelector();` in CSS, return only the first of the matching element.

methods that return one or more elements:
- `getElementByClassName();`
- `getElementByTagName();` h1, li...
- `querySelectorAll();`

- Live nodeLists: when your script updates the page, the nodeList is updated at the same time. Faster to generate. methods that begin with getElementById retun live nodeLists.
- Script nodeLists: methods that begin with querySelector... return static nodeLists.

#### Selecting an element from a nodeList

- item() Method: specify the index number of the element you want as a parameter of the method. Good practise to check the length of the list first. 

`var elements = document.getElementsByClassName('hot')`

`if (elements.length >= 1) {`

` var firstItem = elements.item(0);`

`}`

- Array syntax:

`var elements = document.getElementsByClassName('hot')`

`if (elements.length >= 1) {`

` var firstItem = elements[0];`

`}`

#### Looping through a nodeList

Once a nodeList has been created, a for loop is used to go through each elements ifyou want to apply code to numerous elements.

`var hotItems = document.quesrySelectorall('li.hot');`

`if (hotItems.length > 0){`

` for (va i = 0; i < hotItems.length; i++) {`

` hotItems[i].className = 'cool';`

` }`

`}`

#### Traversing the DOM

When you have an element node, you can select another element in relation with these properties:
- parentNode
- previousSibling
- nextSibling
- firstChild
- lastChild

#### Get-update element content

- `nodeValue` access text from node.
- `textContent` collect or update just the text that is in the containing element and its children.

#### adding or removing HTML content

1.  `innerHTML` retrieve and replace content

2.  DOM manipulation:
  - `createElement()`
  - `createTextNode()`
  - `appenChild()`  

#### Comparing three techniques for dding HTML to a web page

- `document.write()` simple way to add content
- `element.innerHTML` lets you get/update the entire content of any element as a string
- DOM manipulation access, create, update elements and text nodes.

#### Attribute Nodes

Once you have an element node, you can access and change its attributes.

- `getAttribute()` gets the value of an attribute
- `hasAttribute()` checks if hte element node has  specific attribute
- `setAttribute()` sets the value of an attribute
- `remove attribute()` removes an attribute