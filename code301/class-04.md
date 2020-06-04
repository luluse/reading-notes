# Responsive Web Design and Regular Expressions

## CSS GRID

[A complete guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

### Grid items 

`grid-column-start: integer` used alone, the grid item by default will span exactly one column. 

can extend the item across multiple columns by adding the `grid-column-end` property.

desired column width using the `span` keyword. tells how many columns/rows accros.

`grid-column` is a shorthand property that can accept both values at once, separated by a slash.

`grid-row-start` works much like grid-column-start except along the vertical axis.

`grid-area` accepts four values separated by slashes: grid-row-start, grid-column-start, grid-row-end, followed by grid-column-end.

How about multiple items? You can overlap them without any trouble. Use `grid-area` to define a second area

If grid items aren't explicitly placed, they are automatically placed according to their order in the source code. We can override this using the `order` property, which is one of the advantages of grid over table-based layout.

By default, all grid items have an order of 0, but this can be set to any positive or negative value, similar to z-index.

**justify-self**
Aligns a grid item inside a cell along the inline (row) axis (as opposed to align-self which aligns along the block (column) axis). This value applies to a grid item inside a single cell.

### Grid container
you can set the grid up however you like. Apply this property to the direct parent of all grid items
`display: grid;`

  `grid-template-columns: 20% 20% 20% 20% 20%;`

  `grid-template-rows: 20% 20% 20% 20% 20%;`

  `column-gap: 10px;`

  `row-gap: 15px;`

This can be simplified as `grid-template-columns: repeat(5, 20%);`

grid-template-columns/rows doesn't just accept values in percentages, but also length units like pixels and ems. You can even mix different units together.

`.container {`

`justify-items: start | end | center | stretch;`

`align-items: start | end | center | stretch;`

`}`

Aligns grid items along the inline (row) axis (as opposed to align-items which aligns along the block (column) axis). This value applies to all grid items inside the container.

## Responsive Layouts with CSS Grid

[Link to article](https://medium.com/samsung-internet-dev/common-responsive-layouts-with-css-grid-and-some-without-245a862f48df)

## RegExr

Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern

#### Character classes
- `.`	any character except newline
- `\w\d\s`	word, digit, whitespace
- `\W\D\S`	not word, digit, whitespace
- `[abc]`	any of a, b, or c
- `[^abc]`	not a, b, or c
- `[a-g]`	character between a & g
#### Anchors
- `^abc$`	start / end of the string
- `\b\B`	word, not-word boundary
#### Escaped characters
- `\.\*\\`	escaped special characters
- `\t\n\r`	tab, linefeed, carriage return
#### Groups & Lookaround
- `(abc)`	capture group
- `\1`	backreference to group #1
- `(?:abc)`	non-capturing group
- `(?=abc)`	positive lookahead
- `(?!abc)`	negative lookahead
#### Quantifiers & Alternation
- `a*a+a?`	0 or more, 1 or more, 0 or 1
- `a{5}a{2,}`	exactly five, two or more
- `a{1,3}`	between one & three
- `a+?a{2,}?`	match as few as possible
- `ab|cd`	match ab or cd