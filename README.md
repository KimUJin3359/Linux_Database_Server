# Linux_Database_Server

### About
- Database server and client program using a socket
  
  ![미디어1](https://user-images.githubusercontent.com/50474972/114883122-954e5880-9e3f-11eb-8b00-dcc3cd8d52ee.gif)

#### Function(Client)
- connect `IP address` : connect to ip address's server
- save `key`:`value` : send command to server (save it to database)
  ```
  save user:abcdefg
  ```
- read `key` : send command to server (load a data which named key)
  - if save a same key, load the last one
  ```
  save user:abcdefg
  save user:1234
  read user
  >> 1234
  ```
- clear : send command to server (clear a database)
- exit : exit the session

#### Function(Server)
- save : save user's input to database file
- read : read a data which is same tu user's input
- clear : remove a data file
- exit
  ```
  server doesn't mind client's exit or signal
  when server signal(SIGINT), the server will be quit
  ```
