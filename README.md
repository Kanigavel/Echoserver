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
# server code:
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
# client code:
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'kanigavel,3\3\25')
    print(f'Received: {s.recv(1024)!r}')
```

## OUTPUT:
![WhatsApp Image 2025-03-03 at 18 20 30_f851cf54](https://github.com/user-attachments/assets/7fa3ada5-52ee-459e-9fdb-1a8073f297f2)

![WhatsApp Image 2025-03-03 at 18 20 31_3a306300](https://github.com/user-attachments/assets/586cbd8d-73e3-4250-9236-04d690b48c80)


## RESULT:
The program is executed successfully
