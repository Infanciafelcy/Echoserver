# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
Client:
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'INFANCIA FELCY, 212223040067,06-03-2025')
    print(f'Received: {s.recv(1024)!r}')

Server:
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
## OUTPUT:
![image](https://github.com/user-attachments/assets/b40f3f07-bfce-4bd8-b29a-2faa4cdadc7b)


## RESULT:
The program is executed successfully
