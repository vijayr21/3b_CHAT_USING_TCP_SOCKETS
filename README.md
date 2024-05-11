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
server
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
client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUPUT
server![Screenshot 2024-05-11 164720](https://github.com/vijayr21/3b_CHAT_USING_TCP_SOCKETS/assets/149347607/11cde627-3db5-4764-b03a-19f23d7f5b7a)
client![Screenshot 2024-05-11 164726](https://github.com/vijayr21/3b_CHAT_USING_TCP_SOCKETS/assets/149347607/9a73faa3-315c-467d-8ef6-8361ba30c23c)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
