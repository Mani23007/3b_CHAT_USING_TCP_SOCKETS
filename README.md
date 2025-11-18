# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM:

### Client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

### Server:
```python
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
## OUPUT:

### Client:

<img width="780" height="411" alt="client output" src="https://github.com/user-attachments/assets/382746be-b41e-428c-b5db-a3b281af6bae" />

### Server:

<img width="802" height="411" alt="server output" src="https://github.com/user-attachments/assets/39695f2c-9f64-47b5-b5bb-0f225e54c7d4" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
