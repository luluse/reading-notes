## Images ch5 pp94-125


## Color

#### Color can bring your pages to life

3 ways to specify color in CSS:
- color name `h1 { color: Blue; }`. There are 147 color names available.
- Hex code: 6 digit code preceded by a # `h1 { color: #ee3e80; }`
- RGB values tells how much red, green and blue: `h1 { color: rgb(100,100,90) ; }`. RGB values are expressed as number between 0 to 255

`body { background-color: grey ; }`

Color picking tool: colorschemedesigner.com

Make sure the is always enough contrast between background and text.

#### Opacity

Opacity is a value between 0 and 1. Two ways to use it:

- `p { background-color: rgb(100,150,90) ; opacity: 0.5 ; }`
- `p { background-color: rgb(100,150,90) ; background-color: rgba(100,150,90, 0.5) ; }`

#### HSL colors

Hue has values from 0 to 360

Saturation is expressed as a percentage

Lightness is expressed as a percentage

`body { background-color: rgb(100,150,90) ; background-color: hsl(0,100%,100%) ;}`

`/* This is a comment in CSS */`

## Text 

#### Typeface terminology

- serif (extra detail) Georgia, Times, Times New Roman
- Sans-serif (straight ends to letters) Arial, Verdana, Helvetica
- monospace (every letter is the same width) Courier, Courier New

Weight can be: light / medium / bold / black. 
Style can be: Normal / Italic / Oblique.
Stretch can be: condensed / regular / extended/ 

- `font-family` to specify typeface. You can specify a list of fonts separated by commas.
- `font-size` can be specidfied in pixels, % and ems. the default size of text in browser is 16px.
- `@font-face` allows you to use other fonts
- `font-weight` 
- `font-style` Normal, Italic, Oblique
- `text-transformation` uppercase, lowercase, capitalize
- `text-decoration` none, underline, overline, line-through, blink
- `line-height` (leading) adds vertical space between lines of text. 1.4em is considered a good setting.
- `letter-spacing` useful of all uppercase words. em
- `word-spacing` useful when sentence is in bold. em
- `text-align` left, right, centter, justify
- `vertical-align` used with inline elements
- `text-indent` indent the first line of text within an element
- `text-shadow` 

#### Pseudo classes
- `:link` set style for links that have not been visited yet
- `:visited` set style for styles that have been clicked on
- `:hover` changes the appearance when users place their curser over then. Used for links, buttons
- `:active` changes style when a link or a button is being clicked
- `:focus` changes style when an element has focus. 

When pseudo classes are used, they should appear in this order `:link :visited :hover :focus :active`

#### Attribute selectors

- Existence `[]` matches a specific attribute
- Equality `[=]` matches a specific attribute with specific value
- Space `[~=]` matches a specific attribute with whose value appears in a space-separated list of words
- Prefix `[^=]` matches a specific attribute whose value begins with a specific string
- Substring `[*=]` matches a specific attribute whose value contains a specific substring
- Suffix `[$=]` matches a specific attribute whose value ends with a specific string 
