# 2a_Stop_and_Wait_Protocol
## Name:Vedagiri Indu Sree
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
## PROGRAM
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
![image](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/149366776/56e6f0ac-4a34-4ea1-ba1d-c7e37aa28677)
## Server:
![image](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/149366776/4806ea5d-d7a6-43e1-ba1e-4231ce5df322)
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
