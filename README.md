# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
```
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',6000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
```
server.py
import socket 
s=socket.socket() 
s.bind(('localhost',6000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode()) 
```
## OUPUT
<img width="1915" height="1025" alt="{0DC8621A-EB7C-4EF9-8531-42E8A8F7C2C1}" src="https://github.com/user-attachments/assets/c2e40c35-b0bb-4124-a649-749d5d326f60" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
