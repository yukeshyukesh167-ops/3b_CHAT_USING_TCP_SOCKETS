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
### sever side
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
### client side
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
### sever side

<img width="834" height="475" alt="image" src="https://github.com/user-attachments/assets/f33b2212-5e68-4b6b-9351-13492bb002e7" />

### client side

<img width="832" height="467" alt="image" src="https://github.com/user-attachments/assets/3fe2abcd-37fa-45e1-9a90-ec5860a903c4" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
