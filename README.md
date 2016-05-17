# project
socket
'''
    Simple socket server using threads
'''
 
import socket
import sys

HOST = ''   # Symbolic name, meaning all available interfaces
PORT = 5188 # Arbitrary non-privileged port
conn[2]
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
print 'Socket created'
 
#Bind socket to local host and port
try:
    s.bind((HOST, PORT))
except socket.error as msg:
    print 'Bind failed. Error Code : ' + str(msg[0]) + ' Message ' + msg[1]
    sys.exit()
     
print 'Socket bind complete'
 
#Start listening on socket
s.listen(2)
print 'Socket now listening'
 
#now keep talking with the client
while 1:
    #wait to accept a connection - blocking call
    conn, addr = s.accept()
    print 'Connected with ' + addr[0] + ':' + str(addr[1])
    print 'Connected with ' + addr[1] + ':' + str(addr[0])
s.close()
