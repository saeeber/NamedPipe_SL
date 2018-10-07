# Namedpipe communication project for Streamlabs

There are server and client CMake console programs.


They communicate using Namedpipe.

Turn on the server first, and if you execute client, it will be connected automatically.
When the connection established, you can send data from client to server.

Basically, there are three ways to send data.
1. If you want to send some data and save at the server, you can type "save title conetents".
EX) save streamlabs streamlabs made OBS.
Then, server will make a file that title is streamlabs and file contents is streamlabs mad OBS.
If server saved the data successfully, client can get "File Saved" from the server.

2. You can load that you saved. "load title"
EX) load streamlabs
Then, server will load the file that title is streamlabs and will get the contents of the file.
Client can get the contents from server and will show the contents on the client console program.
If server couldn't find the file, client can get "There is no file" from the server.

3. You can send just normal strings and numbers.
EX) abcdefghijklmn123
If client send the strings and numbers, at the server side, you can see the data that client sent.
If it success, client can get "Receive Success" from the server.

