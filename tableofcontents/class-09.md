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