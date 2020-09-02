# Socket.io

### What is the benefit of transforming data into packets?

- optimize the use of the channel capacity available
- minimize the transmission latency
- increase robustness of communication

[Packet switching](https://en.wikipedia.org/wiki/Packet_switching#:~:text=Packet%20switching%20is%20used%20to,to%20increase%20robustness%20of%20communication.)

### UDP is often referred to as a connectionless protocol. Why is this?

- One casts a datagram onto the network with the understanding that it will be delivered on a best-effort basis to whomever it is addressed to. In addition, we accept that there is no notification of a failure, nor can we make assumptions about the sequence of delivery. 
- When a UDP connection occurs, there is no beginning, middle, or end to the conversation. Data simply begins to flow between the two systems.
-  The downfall, of course, is the lack of reliability, so you may have to employ other methods to guarantee delivery.

[Connectionless protocol](https://www.sciencedirect.com/topics/computer-science/connectionless-protocol#:~:text=UDP%20Communications,when%20speed%20is%20an%20issue.)

### Can a socket server application have multiple socket connections?

Yes. A port of a server can be used by many clients (connections)

### Can a socket connection application be connected to multiple socket servers?

A port of a client can be used by a single connection. The reason is a port can be used by a single process, which allocates the port (doing "bind" as a server that will listen to that port for incoming connections, or doing a sort of "open" as a client wanting to do outbound connections from that port out)

[Quora](https://www.quora.com/Can-you-make-a-client-socket-and-a-server-socket-in-one)

### Can an application be both a socket server and a socket connection?

Yes if you use two differen ports or if the sockets won't be using the same port at the same time.


| Term | Definition |
| ------- | ----------------- |
|OSI Model |The Open Systems Interconnection model is a conceptual model created by the International Organization for Standardization which enables diverse communication systems to communicate using standard protocols. In plain English, the OSI provides a standard for different computer systems to be able to communicate with each other.The OSI model can be seen as a universal language for computer networking. It’s based on the concept of splitting up a communication system into seven abstract layers, each one stacked upon the last.|
|TCP Model|The TCP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. The layers are:rocess/Application LayerHost-to-Host/Transport Layer, Internet Layer, Network Access/Link Layer|
|TCP |a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other. |
|UDP | User Datagram Protocol is a connectionless protocol that is designed to stream data.|
|Packets |method of grouping data that is transmitted over a digital network into packets. Packets are made of a header and a payload. Data in the header is used by networking hardware to direct the packet to its destination, where the payload is extracted and used by application software.|
|Socket |Sockets allow communication between two different processes on the same or different machines.|

## Resources

[Web Sockets](https://en.wikipedia.org/wiki/WebSocket)

[Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)

[Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

[Socket.io Documentation](https://socket.io/docs/)

[Socket.io Server API](https://socket.io/docs/server-api)

[Socket.io Client API](https://socket.io/docs/client-api)

[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)