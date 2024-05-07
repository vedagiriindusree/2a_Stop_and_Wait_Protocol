# 2a_Stop_and_Wait_Protocol
## Name: Vedagiri Indu Sree
## Reg No:212223230236
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
## Client:
```
import socket   
s=socket.socket()   
s.bind(('localhost',8000))  
s.listen(5)   
c,addr=s.accept()  
while True:   
i=input("Enter a data: ")   
c.send(i.encode())  
ack=c.recv(1024).decode()   
if ack:   
print(ack)   
continue   
else:   
c.close()  
break
```
## Server:
```
import socket   
s=socket.socket()   
s.connect(('localhost',8000))   
while True:   
print(s.recv(1024).decode())   
s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## Client:
![image](https://github.com/vedagiriindusree/2a_Stop_and_Wait_Protocol/assets/149366776/758856ff-09b8-401d-85a0-c8e65b91015b)
## Server:
![image](https://github.com/vedagiriindusree/2a_Stop_and_Wait_Protocol/assets/149366776/7d1404e2-cb6b-44c6-8b7b-66e3e7768a9b)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
