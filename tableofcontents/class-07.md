# HTML Tables; JS Constructor Functions

## Domain models:
Domain modeling is the process of creating a conceptual model for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model. And a domain model that's articulated well can verify and validate your understanding of that problem.

Bbject-oriented programming in JavaScript at its most fundamental level:
- The `new` keyword instantiates (i.e. creates) an object.
- The constructor function initializes properties inside that object using the `this` variable.
- The object is stored in a variable for later use.

random number generator: `Math.random()`

Steps to follow when building your own domain models:

- When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
- Model its attributes with a constructor function that defines and initializes properties.
- Model its behaviors with small methods that focus on doing one job well.
- Create instances using the `new` keyword followed by a call to a constructor function.
- Store the newly created object in a variable so you can access its properties and methods from outside.
- Use the `this` variable within methods so you can access the object's properties and methods from inside.


## HTML Tables

A table represents information in a grid format.

#### Basic table structure:

`<table>` creates a tble. content is written row by row

`<tr>`indicates the start of a row (table row)

`<th scope="row"></th>` Used like `<tr>`, but represent heading. Can by used for row or column (table heading). You can use the scope attribute to indicate if this heading is for row or column.

`</tr>`

`<tr>`

`<td></td>` represent a cell in that row (table data)

`<td colspan="2"></td>`colspan attribute indicates how many columns that cell should run across. 

`<td rowspan="2"></td>`rowspan attribute indicates how many rows that cell should span down the table. 

`</tr>`

`</table>`

Even when a cell has not data, use <th> or <td> to represent the presence of an empty cell. 


#### Long tables

`<thead></thead>`

`<tbody></tbody>`

`<tfoot></tfoot>`

## Functions, Methods, and Objects

#### Creating an object

**`new`** keyword and the object constructor create a blank object. you can then add properties and methods to the object.

`var hotel = new Object();`

`hotel.name = 'Quay';`

_hotel_ is the object, _name_ is the key and _Quay_ is the value.

#### Updating an object

two ways to assign a new value:
- `hotel.name = 'Park';` 
- `hotel[name] = 'Park';` 

to delete a property: 
- `delete hotel.name;`

to clear the value of a property:
- `hotel.name = '';` set  blank string

#### Create many objects

`function Hotel(name, rooms ,booked){`

`this.name = name;`

`this.rooms = rooms;`

`this.booked = booked;`

`thisckeckAvailability = function(){`

`  return this.room - this.booked;`

` }`

`}`

`This` keyword is used to indicate that the propert or method belongs to the object that `this` function creates.

`var quayHotel = new Hotel('Quay', 40 ,25);`

`Hotel('Quay', 40 ,25);` is the constructor function

#### Arrays 

Arrays are objetcs. They hold a set of key/ value pairs, the **key is the index number**.

### Built-in objects

Toolkit for creating interactive web pages. built-in objets are functionalities commonly needed by manu scripts. Acess these properties using dot notation.

> An object model is a group of objects, where each of them represent related things from the real world. 

Toolkit has 3 compartments:
1. browser object model. creates a model of the browser page or window. topmost object is the **window** object.

- `window.print();`


2. document object model. creates a model of the current webpage. topmost project is the **document** object.

- `document.title`
- `document.getElementById();`
- `document.write();`
- `document.lastModified;`

3. global javascript objects. Do not form a single model.group of individual objects that relate to different parts of the JS language.

- `.length`
- `.toLowerCase`

#### Math object
- `Math.PI;` returns pi
- `Math.round()` rounds number to the nearest integer
- `Math.ceil()` rounds number up to the nearest integer
- `Math.floor()`rounds number down to the nearest integer
- `Math.random()` generate a random number 

#### Date Object

Create a date object: 

`var today = new Date();` 

` var year = today.getFullYear();`

- `getDate()`
- `getFullYear()`

