# Video-Conference-Web-Application
video conference application that will enable  communication between customers and customer representatives.

Build With ->
  simple-peer - Simple WebRTC video/voice and data channels
  socket.io - real-time, bidirectional and event-based communication
  express - web framework for node
  react.js framework

The project is being carried out to a large insurance 
company. A smart screen is created for insurance company customers, where customers 
can receive insurance offers and manage their insurance. At this point, if customers need to 
video chat with customer representatives, this project comes into play.
Insurance business is often complicated. At this point, the customer needs to consult 
someone who has the knowledge of the subject, so the project requires a channel through 
which the customer can reach the customer representative.
 
In the web window, customers will see available customer representatives. When the 
customer presses the Call button, a call will be sent to the relevant customer 
representative. If the customer representative accepts this call, the video conference will 
start and the relevant customer representative will be deleted from the list of available 
customer representatives.
When the video conference ends, the relevant customer representative will be displayed in 
the list of available representatives again.
Since it was a research and development project, I started by researching how a video 
conference works.

I decided that I could do the signaling between client server with socket.io.
Socket.IO was created in 2010. It was developed to use open connections to facilitate 
realtime communication, still a relatively new phenomenon at the time.
 	
Socket.IO allows bi-directional communication between client and server. Bi-directional 
communications are enabled when a client has Socket.IO in the browser, and a server has 
also integrated the Socket.IO package. While data can be sent in a number of forms, JSON is 
the simplest.
To establish the connection, and to exchange data between client and server, Socket.IO 
uses Engine.IO. This is a lower-level implementation used under the hood. Engine.IO is 
used for the server implementation and Engine.IO-client is used for the client.

I used an open source project called simple-peer to stream video between server 
client.Simple Peer is Simple WebRTC video, voice, and data channels.Features of 
simple peer are:
    concise, node.js style API for WebRTC
    works in node and the browser
    supports video/voice streams
    supports data channel

The project consists of two files, server and client. There is a react.js project 
structure on the client side. This structure consists of Home, Client and 
AccountExecutives subfiles. Project have been written with react.js and 
Node.js in VisualCode IDE

There are two rooms on the server side. One for customers and one for customer 
representatives. The signals of customers are collected and managed in the first room, and 
the signals of the customer representatives are collected and managed in the second room.
 
The customer is first welcomed by HomePage and brings the appropriate marked customer 
representatives on the server. When the customer sends a call to any customer 
representative, his video stream goes to the server.
Then it goes from the server to the customer representative. If the customer representative 
accepts the call, the video stream of the customer representative goes to the server and 
from the server to the customer
