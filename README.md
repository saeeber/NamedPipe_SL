# Namedpipe communication project for Streamlabs

There are a server and a client CMake console programs.

Each EXE files are in each directories "server/build/src/Release/" and "client/build/src/Release/".

Source codes are in each directories "server/src/" and "client/src/".

Or you can open the solutions using "server/build/SERVER.sln" and "client/build/CLIENT.sln" on the Visual Studio


They communicate using Namedpipe.

Turn on the server first, and if you execute client, it will be connected automatically.
When the connection established, you can send data from client to server.


Basically, there are three ways to send data.
1. If you want to send some data and save at the server, you can type "save title contents".

EX) save streamlabs streamlabs made OBS.

Then, the server will make a file that title is streamlabs and file content is "streamlabs mad OBS".
If the server saved the data successfully, the client can get "File Saved" from the server.


2. You can load that you saved. "load title"

EX) load streamlabs

Then, the server will load the file that title is streamlabs and will get the contents of the file.
The client can get the contents from the server and will show the contents on the client console program.
If the server couldn't find the file, the client can get "There is no file" from the server.


3. You can send just normal strings and numbers.

EX) abcdefghijklmn123

If the client sends the strings and numbers, at the server side, you can see the data that the client sent.
If it success, the client can get "Receive Success" from the server.

