# TCP-client-server-using-winsock

run:

```MinGW
g++ server.cpp -o server.exe -lws2_32
g++ client.cpp -o client.exe -lws2_32
```

```server.cpp
.\server.exe
```


```client.cpp
.\client.exe localhost
```
Input: "hello" --> client.cpp

Output:
```
Bytes Sent: 5
Bytes received: 5
Connection closed
```