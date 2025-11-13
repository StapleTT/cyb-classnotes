# Nmap commands

# Overview
- Nmap: network mapper
- nmap = networkmapper
- Using to scan on local network
- Helps us locate devices that we may or may not know about
- Gives us back useful information such as IP addresses, MAC addresses, hostnames, and much more
- Diferent Levels of scanning (1-5)
    Goes from quieter -> louder

# Installation
sudo apt install nmap

# Basic commands
- nmap <ipaddr>
    nmap 192.168.1.0
    nmap scanme.nmap.org
- nmap localhost = scans your target machine
    allows you to see what ports you have available on your device
    total ports: 65535

- nmap -p <portnumbers> <ipaddr>
- scans an ip and the ports listed
    nmap -p 1-5000 192.168.1.1

- nmap -sL
    scans for a list of hosts (may not actually be up)

- nmap -sn
    ping scan, does not scan for port openings
    like knocking on a door to see if anyone is home

- nmap -sn <ipaddr>/<range>
    scans for and discovers all available hosts on a network based on a range
    EX: sudo nmap -sn 192.168.1.0/24
    grabs back the mac addresses, ip addresses, and estimated name/type of device
    need to know your ip address and the nework range for accuracy
