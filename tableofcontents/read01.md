# Introductory HTML and JavaScript
 
## Structure
 
> HTML describes the structure of pages. HTML code made up of characters living inside angled brackets to give the information they surround special meaning.
 
`<h1>` : This is a tag
 
`</h1> `: This is a closing tag
 
`<h1>Your title here</h1>` : This is an element
 
> Tags act like containers.
 
`<p lang=”en-us”>` :
**lang** is the attribute name,
**en-us** is the attribute value
 
The <head> element contains information about the page.
 
Everything written in the <body> element will appear on the main browser window.
 
## Extra Markup
 
Always start HTML with `<!DOCTYPE html>`
 
`<!-- This is a comment -->`
 
Use Id attribute to uniquely identify elements on the page.
`<p id=”quote”>`
 
Class attribute is a way to identify several elements as being different from the other elements on the page.
 
Id and Class attributes only change their appearance if there is a CSS rule attached.
 
Block elements start on a new line in the browser window. `<h1>` `<p>` `<ul>`
 
Inline elements continue on the same line. `<a>` `<b>` `<img>`
 
`<div>` element allows you to group a set of elements together.
 
`<span>` acts like an inline equivalent of `<div>`.
 
 
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
 
 
## Programming with JavaScript
 
JavaScript allows to make web pages more interactive in 4 ways:
- Access the content of the page
- Modify the content of the page
- Program rules and instructions
- React to events
 
### What is a script?
 
> A script is a series of instructions that a computer can follow to achieve a goal.
 
To write a script you need to state your goal and list the tasks that need to be completed in order to achieve it:
- Define the goal
- Design the script (write down each individual steps the computer needs to perform)
- Code each step
 
You can use a flowchart to help you visualize each step.
 
### How do computers fit in with the world around them?
 
- Objetcs: each physical thing in the world can be represented as an object.
 
- Properties (characteristics):
Each property has a name and a value.
 
- Events: programs are designed to do different things when users interact with the computer in different ways.
 
- Methods: methods represent things people need to do with objetcs and it will change the value of the object's property.
 
#### The document object represents an HTML page
 
like other objetcs, the document object has:
 
- properties: characteristics of the current page.
- methods: performs tasks associated with the document.
- events: You can respond to events, such as user clicking or tapping on an element.
 
 
### How do I write a script for a web page?
 
JS is the behavior layer. This is where you add the interactivity.
 
As good practise, link your JS file at the end of the body in your HTML sheet so it won’t affect too much the loading time for the rest of the info on your site.
Use this element : `<script src=”yourfile.js”></script>`
 
 
#### How to use objects and methods
 
`document.write(‘Good afternoon’);`
 
- Document is the object and represents the entire web page.
- . is the member operator
- write() is the method of the object
- ‘Good afternoon’ is the parameter of the method. This is the piece of info that is going to be displayed.

