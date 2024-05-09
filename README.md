# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name:Roshini.S
## Reg.No:212223230174
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
## Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
clientMessage=c.recv(1024).decode()
c.send((clientMessage.encode()))
```
## Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("client>")
s.send(msg.encode())
print("server>",s.recv(1024).decode())


```
## OUPUT
## client:
![image](https://github.com/23008859/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139117979/7ca746f5-70ab-4c18-879b-bd8ae453444c)

## server:
![image](https://github.com/23008859/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139117979/9d8d9f8e-20f9-44fe-9c8e-98a7d8c50577)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
