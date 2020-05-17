import socket

s= socket.socket()


server_ip="192.168.225.176"
s.connect((server_ip,1634))


data1 = s.recv(1024)
print(data1)
i = input()
#print("here")
#print(i)

if(i=='1'):
    #print("ajith")
    s.send(bytes(i,'utf-8'))
    data2 = s.recv(1024)
    file=input(data2)
    s.send(bytes(file,'utf-8'))

    timestamp=s.recv(1024)
    print(b"The timestamp of the modified file is",timestamp)
    
if(i=='2'):
    #print(i)
    s.send(bytes(i,'utf-8'))
    data3 = s.recv(1024)
    print(data3)
    
    filename = input()
    s.send(bytes(filename,'utf-8'))
    
    with open(filename,"rb") as f:
        l=f.read(1024)
  
    
        while (l):
            s.send(bytes(l))
            l=f.read(1024)
    f.close()  
    
    data4=s.recv(1024)
    print(data4)


#s.close()