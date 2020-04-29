## HTML Links

Links are created using the `<a href=""></a>` element. The text between the opening and closing tag is called **link text**.

Linking to other websites: the value of the href attribute will be the full web address for the site. it is known as **absolute** URL.

Linking to other pages on the same site: use the **relative** URL. The href attribute is just the name of the file if all the pages are in the same folder.
- same folder: use fileName.html
- child folder: use nameOfTheChildFolder/fileName.html
- grandchild folder: use childFolder/grandChildFolder/fileNAme.html
- parent folder: use ../FileName.html
- grandparent folder: use ../../fileName.html

Email links:
- `<a href="mailto:lulu@gmail.com">Email Lulu</a>`

opening links to a new window:
- add attribute `target=_blank` in the `<a>` tag.

Linking to a specific part of same page:
- add list of contents at the top of page
- add an Id attribute to sections you want to link.