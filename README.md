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

    client
    server
    client
    2a_Stop_and_Wait_Protocol
    AIM
    ALGORITHM
    PROGRAM
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
    import socket
    s=socket.socket()
    s.connect(('localhost',8000))
    while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
## OUTPUT
##client
![Screenshot 2025-04-21 214041](https://github.com/user-attachments/assets/b65f9b11-99b7-45a6-b82d-fb189d5d97b9)

##server
![Screenshot 2025-04-21 214047](https://github.com/user-attachments/assets/d2c1a7b7-3646-47c0-8d38-272aa52816e9)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
