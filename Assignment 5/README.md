# Assignment 5 : Network Server Program

This Assignment it to implement a network server program.

Program V1 Specifications
  -   Load CSV database file scifi.csv and store
  -   Perform required socket operations to createand bind a socket
  -   Listen for clients at TCP port 12345
  -   When a client successfully establishes connection, send a message with contents HELLO
  -   Wait for message from client
  -   Perform following based on received message from client:
      -   If the message has contents 'BYE' (case-insensitive), close connection to client and go back to listening at the port
      -   If the message has the contents 'GET' (case-insensitive), send a message back containing the entire database. Go back to waiting for a message.
      -   If the message has the contents 'GET' (case-insensitive) follwoed by a number (eg. 'GET 12'), treat the number as the row number of the record to be fetched. Send a message back containing the record at the specified row number. If it does not exist, send back 'ERROR'. Go back to waiting for a message.
      
Program V2 Specifications
  -   After connecting to client, fork a child process. Upon successful fork, the parent goes back to listening while the child does the rest (communicating with  client)
  -   If fork is unsuccessful the process should communicate with the client.
  
Makefile
  -   Automatically build the program
      -   'dbserver' compiles V1 Program
      -   'dbserverFork' compiles V2 Program
      -   'clean' delete any compiled files created by the program 
