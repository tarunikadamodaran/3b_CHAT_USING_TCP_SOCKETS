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
**CLIENT:**
 ```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

**SERVER:**
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

## OUTPUT:

**SERVER:**

![image](https://github.com/tarunikadamodaran/3b_CHAT_USING_TCP_SOCKETS/assets/145633268/be68ce18-3ebc-4ed8-9512-e44012ed1ab3)



**CLIENT:**


![image](https://github.com/tarunikadamodaran/3b_CHAT_USING_TCP_SOCKETS/assets/145633268/abb7b812-d5a4-4696-b6de-e5616711d62d)




## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
