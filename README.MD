========================
There are 5 source files and 1 index file
src/cloudsearch/_0CommunicationInterface.java is the abstract class of communication interface
src/cloudsearch/_1SocketCommunication.java is an implementation of communication class (with Java Socket)
src/cloudsearch/_2commonFn.java is a common utility, setting used by both client and server
src/cloudsearch/_3Server.java is a specific code for server
src/cloudsearch/_4Client.java is a specific code for client

index/Index.txt is the index file that server code will try to read
========================
To compile without IDE,

go to src folder (not in cloudsearch folder)
javac ./cloudsearch/_3Server.java 
javac ./cloudsearch/_4Client.java 
====
To run without IDE,
%% run server 
java cloudsearch._3Server

%% run client 
java cloudsearch._4Client
=======================
Things to do:
1) currently _2commonFn.java specify the address as localhost:1350. Modify it and try to run client and server on different machines.
2) create new _1XXXCommunication.java and register it in _2commonFn.java's newCommunicator function. Try to limit the modification to other files. Some functions in _0CommunicationInterface can be left empty if it make sense to do so.
====
NOTE: delete all .class files in src/cloudsearch before recompile with modified source code. Otherwise, java may use some of the old .class rather than making the new modified one
====
