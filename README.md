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
'''
Server.py
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

Client.py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
'''
## OUPUT
'''
<img width="785" height="201" alt="image" src="https://github.com/user-attachments/assets/847d9c45-1527-431a-b44e-474929f4a0c4" />
<img width="779" height="167" alt="image" src="https://github.com/user-attachments/assets/9bdf3a82-73ee-4bc7-ba29-be9e565c73e8" />

'''
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
