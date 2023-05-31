# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :

AIM:

To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

ALGORITHM:

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will
send NACKsignal to client.
6. Stop the program


PROGRAM:

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
SERVER:
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
OUTPUT:

CLIENT:

![image](https://github.com/Subalakshmisuresh/EX-8/assets/121957896/0eabcea5-e7ce-42c8-bad7-c2161dd396d9)

SERVER:

![image](https://github.com/Subalakshmisuresh/EX-8/assets/121957896/ee45890c-c3e2-4b95-a736-c0f31e88e3d3)

RESULT:

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed
