# Message Queues

### What does it mean that web sockets are bidirectional? Why is this useful?

WebSocket allows a single TCP socket connection to be hijacked so that the client-server relationship can relay bi-directional, full-duplex (or sometimes also referred to as double-duplex) messages instantaneously.

[WebSocket: Simultaneous Bi-Directional Client-Server Communication](https://medium.com/@nerdplusdog/websocket-simultaneous-bi-directional-client-server-communication-e7948203054b)

### Does socket.io use HTTP? Why?

- HTTP doesn’t allow for bi-directional communication between a server and a client.
- WebSocket is a new type of communications protocol that is different from HTTP.
- WebSocket is designed to run on HTTP ports 80 and 443, and supports HTTP proxies and intermediaries. By doing so, WebSocket is compatible with HTTP protocol. In order to achieve this compatibility, the WebSocket handshake uses the HTTP Upgrade header to switch from the HTTP protocol to the WebSocket Protocol.

### What happens when a client emits an event?

- transmitting data to the server.
- to do it: call the WebSocket object's send() method for each message you want to send 

### What happens when a server emits an event?

- send a message over to client
- a message event is sent to the WebSocket object. To handle it, add an event listener for the message event, or use the onmessage event handler. To begin listening for incoming data, you can do something like this: 
```
exampleSocket.onmessage = function (event) {
  console.log(event.data);
}
```

[WebSocket client application - MDN](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_client_applications)

### What happens if a client “misses” an event?

Unhandled messages are just ignored. Nothing happens with it. 

### How can we mitigate this?

You could avoid missing messages by always having the handlers installed and then deciding in the handlers whether to do anything with the message or not.

[Stack overflow](https://stackoverflow.com/questions/32816290/what-happens-with-unhandled-socket-io-events)

### Term

| Term | Definition |
| ------- | ----------------- |
|Web Socket |The WebSocket object provides the API for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.|
|Socket.io|Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server.|
|Client|client has to start the WebSocket handshake process by contacting the server and requesting a WebSocket connection.|
|Server|server must listen for incoming socket connections using a standard TCP socket|