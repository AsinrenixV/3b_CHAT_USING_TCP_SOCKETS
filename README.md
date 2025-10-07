# 3b.CREATION FOR CHAT USING TCP SOCKETS
## REG NO : 212224040036
## NAME : ASIN RENIX V
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
```
server.py
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
<img width="1735" height="252" alt="image" src="https://github.com/user-attachments/assets/25fcc7f4-bc09-426c-8826-ede873212c90" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
