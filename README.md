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
server.py
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
client.py
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
<img width="741" height="168" alt="Screenshot 2026-03-11 085636" src="https://github.com/user-attachments/assets/d4c0e513-239f-49dc-9205-93b009adffe0" />

<img width="737" height="170" alt="Screenshot 2026-03-11 085641" src="https://github.com/user-attachments/assets/c9ee3785-3355-4815-bfff-9a6f3cd05f2f" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
