# 2a_Stop_and_Wait_Protocol
PRASANNA A
212223220078
B Tech IT
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
```import socket

s=socket.socket()

s.bind(('localhost',8000))

s.listen(5)

c,addr=s.accept()

size=int(input("Enter number of frames to send: "))

l=list(range(size))

s=int(input("Enter Window size:"))

st=0

i=0

while True:

 while(i<len(l)):
 
   st+=s
    
   c.send(str(l[i:st]).encode())
    
   ack=c.recv(1024).decode()
     
   if ack:
         
   print(ack)
         
   i+=s
   
```   
PROGRAM FOR SERVER:

```import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

print(s.recv(1024).decode())

   s.send("acknowledgement recived from the server".encode())
```


  ##OUTPUT

![Screenshot 2024-02-27 140647](https://github.com/aswethaashok/2a_Stop_and_Wait_Protocol/assets/149987410/af2dc450-b57f-4d39-9684-16f0311e9416)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
