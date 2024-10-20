# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
# client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
# server:
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
## OUPUT
# client:
![Screenshot 2024-10-20 152512](https://github.com/user-attachments/assets/f9a0294c-9519-4838-9232-23448a4e8702)
# server:
![Screenshot 2024-10-20 152519](https://github.com/user-attachments/assets/9b96affa-da47-4208-828a-95a1c7f21ab9)

## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.
