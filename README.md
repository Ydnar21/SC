# SC
Server Client simple
#Client

import socket
import json
HOST = '127.0.0.1'  # The server's hostname or IP address
PORT =  1035  # The port used by the server


# Create a socket object
s = socket.socket()        
 
# Define the port on which you want to connect
             
 
# connect to the server on local computer
s.connect((HOST, PORT))
 
# receive data from the server and decoding to get the string.


user_input = " "
while user_input != "exit":
    user_input = input("Enter the stock you would like to evaluate: ")   
    s.send(user_input.encode())
# close the connection
s.close() 
