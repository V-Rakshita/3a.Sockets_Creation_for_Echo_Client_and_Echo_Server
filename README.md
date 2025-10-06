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
### Server side:
```python
import socket 
s=socket.socket() 
s.bind(('localhost',5500)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
### Server side output:
<img width="785" height="31" alt="image" src="https://github.com/user-attachments/assets/87d88f7f-780d-4952-82c7-960c6e56ed12" />

### Client side:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',5500)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### Client side output
<img width="723" height="211" alt="image" src="https://github.com/user-attachments/assets/6365d4c3-f023-44f9-8999-1054c644757f" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
