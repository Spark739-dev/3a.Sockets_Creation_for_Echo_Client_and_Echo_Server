# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name: VESHWANTH.
## REG NO: 212224230300
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
  ## CLIENT:
      import socket
      s=socket.socket()
      s.connect(('localhost',8000))
      while True:
        msg=input("Client>")
        s.send(msg.encode())
        print("Server > ",s.recv(1024).decode())

  ## SERVER:
      import socket
      s=socket.socket()
      s.bind(('localhost',8000))
      s.listen(5)
      c,addr=s.accept()
      while True:
          ClientMessage=c.recv(1024).decode()
          c.send(ClientMessage.encode())



## OUPUT
  ## CLIENT:
![CN EXP 3A CLIENT](https://github.com/user-attachments/assets/76ca41b2-b14d-4b0e-afdc-50e6d5acf789)
  ## SERVER:
![CN EXP 3A SERVER](https://github.com/user-attachments/assets/56d54d4c-34fd-42e6-9ad5-2fcede3f74f6)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
