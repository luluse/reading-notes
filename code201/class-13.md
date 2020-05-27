# Local Storage

What we want is:

- a lot of storage space
- on the client
- that persists beyond a page refresh
- and isn’t transmitted to the server

> problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

Web storage refered to as “HTML5 Storage”, “Local Storage” or “DOM Storage.” 
- It’s a way for web pages to store named key/value pairs locally, within the client web browser.
- this data is never transmitted to the remote web server.
- it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

Using HTML5 Storage
- based on named key/value pairs.
- data is stored as a string.
- If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

Tracking changes to the HTML5 storage area:

- storage event is fired on the window object whenever setItem(), removeItem(), or clear()
- you can trap the storage event
- Trapping the storage event works the same as every other event you’ve ever trapped.

Storage event objects:
- property: key / type: string / the named key that was added, removed, or modified
-  oldValue / any / the previous value (now overwritten), or null if a new item was added
- newValue / any / the new value, or null if an item was removed
- url / string / the page which called a method that triggered this change

HTML5 storage in action

> Before HTML5, If you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself.

- use function saveGameState()
- On page load, instead of automatically calling a newGame() function, we call a resumeGame() function instead. 
- Using HTML5 Storage, the resumeGame() function checks whether a state about a game-in-progress is stored locally. If so, it restores those values using the localStorage object.