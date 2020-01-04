# Socket Programming, Threads, and Synchronization

This is a rudimentary **multi-threaded** chatting application. The application will run on a client/server model which means there are two different programs: a server and a client i.e. server will be running and multiple clients can connect to the server and chat to each other using this server program as an intermediary. The server and clients may run on the same PC or on different ones.

### Features:
- The server program creates a socket and starts listening on the port passed to it at command line.
- The client makes a socket and tries to make a connection to server program using the servers PCs IP and the port number the server is listening on. Once the connection is established, the client sends its identifier. In case there is no server running, the client should terminate with an appropriate message.
- The server program accepts connections from multiple clients. For each connection established, the server stores the client's identifier and communication port. Sever creates a separate thread for each connection with the client.
- If a new connection request comes from a a client with a client identifier which is already in use, the server informs the client with an appropriate error message and close that connection.
- Commands server entertains:
	1. **/list** - the server puts the names of all the clients connected to itself in string and send it back to the client to display to user.
	1. ** /msg** – users can type this command to send messages to other clients.
	1. ** /quit **– users can type this command to disconnect from the server and quit the client.
