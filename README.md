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

## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
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
 c.send(ClientMessage.encode())
```

## OUTPUT

## CLIENT
![243808843-4df0136b-a680-453b-90ac-47d33d661ae7](https://github.com/Jai-1801/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139335300/945eb049-dd59-41ec-beaf-bf89449d403d)

## SERVER
![243808859-9d992ebc-c693-459b-84a0-ba0a74a59131](https://github.com/Jai-1801/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139335300/4a2eb9f6-50c1-48fd-ac91-d96264deb03e)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
