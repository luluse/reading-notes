# Forms and Events

## Forms

Adding text:
- text input (single line)

`<input type="text" name="username" maxlength="30" /> `

- passsword input

`<input type="password" name="password" maxlength="30"/ > `

- text area (multi-line)

`<textarea name="comments" cols="20" rows="4"></textarea> `

Making choices:
- Radio buttons

`<input type="radio" name="" value="" /> `

- checkboxes

`<input type="checkbox" name="" value="" /> `

- drop-down boxes

`<select name="">`
`<option value=""></option>`
`<option value=""></option>`
`</select>`

Submitting forms:
- Submit buttons

`<input type="submit" name="" value="" /> `

- Image buttons

Uploading Files:
- File upload

Form Structure:

`<form></form>`
- action attribute: its value is the URL for the page on the server that will receive the information when the form is submitted.
- method attribute: values can be **get** or **post**

#### HTML5
- Form validation `<required="required">`
- Date input `<input type="date" name="" /> `
- Email and URL input `<input type="email" name="email"/> ` `<input type="url" name="website" /> `

## Lists, Tables and Forms

- bullet point style `ol { list-style-type:}`
- positionning the marker `ul {list-style-position: }` Value can be **inside** or **outside**

#### Table properties

- give cells padding
- distinguish headings
- shade alternate rows
- align numerals

#### Styling forms
 Most common to style:
 - text input
 - text area
 - submit buttons
 - labels on forms

 ## Events

Events are the broswer's way of indicating when something has happened.

#### Event handling:
1. select element you want the script to respond to.
2. Specify event that will trigger the response. (biding an event to the DOM)
3. call code you want to run when the event occurs.

DOM level 2 event listeners:

`element.addEventListener('event', functionName);`
- element is the element node to target.
- event to bind nodes to in quote marks
- name of function to call to run code. parentheses are ommited

#### Event flow
- Event bubbling: the event starts at the most specific node and flows outward to the least specific one. 
- Event capturing: the event starts at the least specific node and flows outward to the most specific one. 

#### changing default behavior
- preventDefault() 
- stopPropagation()

#### UI Events
- load
- unload
- error
- resize
- scroll

#### Keybord Events
- keydown
- keyup
- keypress

#### Mouse Events
- clicki
- dlbclick
- mousedown
- mouseup
- mousemove
- mouseover
- mouseout

#### Focus Events
- focus / focusin
- blur / focusout

#### Form Events
- input
- change
- submit
- reset
- cut
- copy
- paste
- select

