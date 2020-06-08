# REST

### "A Conversation about REST with my brother"

- REpresentational State Transfer. It is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other.

- The whole world wide web is built on an architectural style called “REST”. REST provides a definition of a “resource”, which is what those things point to.

- A web page is a “representation” of a resource. Resources are just concepts.

- URLs tell the browser that there's a concept somewhere. Specifically, the browser asks for the web page representation of the concept

- “Web Services” or "APIs". The basic concept is that machines could use the web just like people do.

- We need some way of having one machine tell another machine about a resource that might be on yet another machine.

- The URL let machines tell to each other where things are. It let's all of these systems tell each other about each other's nouns.

- Verbs are important. There's a powerful concept in programming and CS theory called “polymorphism”. Different nouns can have the same verb applied to them.

- HTTP is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.

- GET is a pretty important verb. Especially when you're using a web browser because browsers pretty much just GET stuff.

- If one system needs to add something to another system, it would use an HTTP POST.

-  If a system wants to replace something in another system, it uses an HTTP PUT. 

- Only thing left to figure out is what the data models should look like. Now, we just tell Rails what we want our data to look like, and it takes care of all of the communication pieces for us.

### SuperAgent

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request

