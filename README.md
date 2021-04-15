# Linux_Database_Server

### About
- Database server and client program using a socket
  
  https://user-images.githubusercontent.com/50474972/114882800-4accdc00-9e3f-11eb-9609-b89950424557.mp4




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
