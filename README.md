# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client>")
 s.send(msg.encode())
 print("Server>",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client>",ClientMessage)
 msg=input("Server>")
 c.send(msg.encode())
```
## OUPUT
## CLIENT
![Screenshot 2024-09-21 103925](https://github.com/user-attachments/assets/d9121e64-236f-4808-95d7-67d1dd59d334)

## SERVER
![Screenshot 2024-09-21 104002](https://github.com/user-attachments/assets/3ea4dbdb-e1a9-463d-b32d-91ade50ca9f1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
