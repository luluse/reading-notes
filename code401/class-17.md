# TCP Servers

### Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?

- a new connection
- error event
- newListener



### Why are events sometimes better than asynchronous actions with callbacks?

The events raised by event emitters are synchronously executed by the listeners in the current event loop’s iteration.

With an event emitter, we can simply raise a new event from a different part of an application, and a listener will listen to the raised event and have some action performed for the event.

- [Node Event Emitters](https://medium.com/developers-arena/nodejs-event-emitters-for-beginners-and-for-experts-591e3368fdd2)
- [Phases of the Node JS Event Loop](https://medium.com/@kunaltandon.kt/process-nexttick-vs-setimmediate-vs-settimeout-explained-wrt-different-event-loop-phases-c0506b12921d)

### What does an EventEmitter instance do?

EventEmitters emit the event 'newListener' when new listeners are added and 'removeListener' when existing listeners are removed.

EventEmitter instance will emit its own 'newListener' event before a listener is added to its internal array of listeners.

EventEmitter is a class that helps us create a publisher-subscriber pattern in NodeJS.
- [Node.js Event Emitter](https://www.tutorialspoint.com/nodejs/nodejs_event_emitter.htm)

### When is a program’s call stack, event queue, and event loop active?
A program’s call stack, event queue, and event loop are active as soon as the program starts.


| Term | Definition |
| ------- | ----------------- |
|Observer Pattern |Observer pattern offers a subscription model in which objects subscribe to an event and get notified when the event occurs|
|Listener|function objects called by emitters(named events)|
|Event Handler|callback function that will be called when an event is triggered|
|Event Driven Programming|logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision|
|Event Loop|keeps running continuously and checks the Main stack, if it has any frames to execute, if not then it checks Callback queue, if Callback queue has codes to execute then it pops the message from it to the Main Stack for the execution.|
|Event Queue|Where event handlers are stored until executed|
|Call Stack| all your javascript code gets pushed and executed one by one as the interpreter reads your program, and gets popped out once the execution is done. |
|Emit/Raise/Trigger|event is emitted any time a listener is added. When this event is triggered, the listener may not yet have been added to the array of listeners for the event. With an event emitter, we can simply raise a new event from a different part of an application, and a listener will listen to the raised event and have some action performed for the event.|
|Subscribe|EventEmitter is a class that helps us create a publisher-subscriber pattern in NodeJS|



## Resources

[OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)

[OSI Model](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

[What is TCP](https://searchnetworking.techtarget.com/definition/TCP)

[Build a TCP Server (code only)](https://techbrij.com/node-js-tcp-server-client-promisify)

[Node docs: net module](https://nodejs.org/api/net.html)

[Observer pattern](https://www.dofactory.com/javascript/design-patterns/observer#:~:text=The%20Observer%20pattern%20offers%20a,event%20driven%20programming%2C%20including%20JavaScript.&text=The%20event%20and%20event%2Dhandler,of%20the%20Observer%20design%20pattern.)

[Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming#:~:text=An%20Event%20Handler%20is%20a,event%20handler%20for%20that%20event.)