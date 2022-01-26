# SC
Server Client simple
#Server script


from asyncore import read
import os
from urllib import response,parse
import urllib.request
from urllib.request import Request, urlopen
import urllib
import socket 




s=socket.socket()# creates a new socket



PORT = 1035  #5Port to listen on (non-privileged ports are > 1023)

s.bind(('',PORT))

print("socket binded to %s" %(PORT))


# put the socket into listening mode
s.listen()    
print ("Socket is listening")  


c, addr = s.accept()
with c:
    print('Connected by', addr)
    while True:
        data = c.recv(1024).decode()
        print(data)
        if not data:
            break
        
s.close()
