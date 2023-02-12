# Structure web pages with HTML

## Process and design

> Every website should be designed for the target audience

When you figured out what needs to appear on your site: 
- Start to organize the information into sections. 
- Create a site map (a diagram of the pages to plan the structure of the website).
- Create a wireframe (sketch of key infos for each page- shows the hierarchy of the info).
- Organize infos on the page.
- Use a visual hierarchy to create contrast and communicate information (size/color/style).
- Consistency is key.
- Have a good navigation (concise, clear, selective, interactive). 

## Structure

> HTML describes the structure of pages
HTML code made up of characters living inside angled brackets to give the information they surround special meaning. 

`<h1>` : This is a tag

`</h1> `: This is a closing tag

`<h1>Your title here</h1>` : This is an element

> Tags act like containers. 

`<p lang=”en-us”>` :
**lang** is the attribute name,
**en-us** is the attribute value

## HTML5 Layout

HTML5 is a set of elements that define the structure of a page.

Header and footer live within the body of the document.

`<body>`

`<header></header>`

`<footer></footer>`

`</body>`

`<article></article>` acts as a container for any section of the page that could stand alone. 

`<aside></aside>` when under `<article>`, should contain info related to the article. When alone, act as a container.

`<section></section>` groups related content

`<div></div>` groups together related elements

## Extra Markup

Always start HTML with `<!DOCTYPE html>`

`<!-- This is a comment -->`

Use Id attribute to uniquely identify elements on the page. 
`<p id=”quote”>`

Class attribute is a way to identify several elements as being different from the other elements on the page. 

Id and Class attributes only change their appearance if there is a CSS rule attached. 