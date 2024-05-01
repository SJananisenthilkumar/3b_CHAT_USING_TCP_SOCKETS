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

Developed by : JANANI S

REG NO : 212223230086

Client 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
Server
```
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
Client
![image](https://github.com/SJananisenthilkumar/3b_CHAT_USING_TCP_SOCKETS/assets/144871139/0db76e84-ea7f-4959-a170-4316e7110eec)

Server
![image](https://github.com/SJananisenthilkumar/3b_CHAT_USING_TCP_SOCKETS/assets/144871139/4193e6ab-c850-4e74-a128-027ae652a729)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
