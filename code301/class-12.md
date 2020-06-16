# Components

Use case for Partials is a reusable piece of code like a nav bar or a header etc. 

## [EJS Partials](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)

> Partials come in handy when you want to reuse the same HTML across multiple views.

- create a views/partials/ directory
- In this directory create file called navbar.ejs which will contain only the HTML for the navigation bar at the top of the home and post pages. Same for header and footer
- Now our partials are defined
- In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters
- Including a partial in EJS is quite straightforward. You use `<%- include( PARTIAL_FILE ) %>` where the partial file is relative to the template you use it in.
