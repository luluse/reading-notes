## Introducing CSS

Css works like an invisible box around every HTML element. It allows you to create rules that control the way that each individual box is presented. 

- Css works by associating rules with HTML elements. A CSS rule contain two parts: 

    `P {font-family: Arial;}`  where `P` is the selector and `{font-family: Arial;}’ is the declaration.

- a CSS declaration contain a property and a value separated by a colon :

    `{font-family: Arial;}’ where `font-family’ is the property and `Arial’ is the value.

### How to link you CSS sheet to your HTML sheet :

`<link href=”styles.css” type=”text/css” rel=”stylesheet” />` This element lives inside the head of your HTML sheet.

### Commonly used selectors:

- Universal selector `* {}` Targets all elements on the page
- Class selector `.note {}` Targets any element whose class attribute has a value of note.
- ID selector `#introduction {}` Targets elements whose id attribute has a value of introduction. 

### Advantages to place CSS rules in a separate style sheet:

- All of your web pages can share the same style sheet
- Website will load faster
- Easier to edit and update
- Good practice, keeps HTML sheet easier to read



## Color can bring your pages to life

### 3 ways to specify color in CSS:
- color name `h1 { color: Blue; }`. There are 147 color names available. 
- Hex code: 6 digit code preceded by a # `h1 { color: #ee3e80; }`
- RGB values tells how much red, green and blue: `h1 { color: rgb(100,100,90) ; }`. RGB values are expressed as number between 0 to 255

`body { background-color: grey ; }`

Color picking tool: colorschemedesigner.com

Make sure the is always enough contrast between background and text.

### Opacity

Opacity is a value between 0 and 1. Two ways to use it:

- `p { background-color: rgb(100,150,90) ; opacity: 0.5 ; }` 
- `p { background-color: rgb(100,150,90) ; background-color: rgba(100,150,90, 0.5) ; }` 

### HSL colors

Hue has values from 0 to 360

Saturation is expressed as a percentage

Lightness is expressed as a percentage

` body { background-color: rgb(100,150,90) ; background-color: hsl(0,100%,100%) ;}`


### `/* This is a comment in CSS */`