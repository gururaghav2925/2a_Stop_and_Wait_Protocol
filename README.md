# 2a_Stop_and_Wait_Protocol

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

server.py

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())


client.py

import socket 
s=socket.socket() 
s.bind(('localhost',8000)
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

## OUTPUT
![Screenshot 2024-02-28 143524](https://github.com/gururaghav2925/2a_Stop_and_Wait_Protocol/assets/151489500/1d4c1073-95a5-477c-a7fc-41d357922524)

![Screenshot 2024-02-28 143533](https://github.com/gururaghav2925/2a_Stop_and_Wait_Protocol/assets/151489500/5a146fc1-3416-433c-bc23-ec3b28c8e1a4)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

