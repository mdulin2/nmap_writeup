# Nmap

## Introduction
Nmap is a free network scanner, that has an amazing variety that people can use.  
Just to begin, it can scan for open ports, versions of the server, scan whole subnets, check particular ports things...  Nmap is an extremely versitle tool.

## Installation
I would run this is a Linux virtual machine, in the terminal. So, that's how I'm going to explain it here.  
Simply run:
```
sudo apt-get install nmap
```
and this should install it on ubuntu or Debian it should work. Kali Linux should already have a preinstalled set up of it on there. Other OS's installing nmap are defintely possible; just google or ask me if you have issues.

## Terminal
To run nmap type this into the terminal:
```
nmap
```
This will open up the help screen for running nmap. 

## Knowledge
### Ports
There are a few base things that need to be known before this will be understandable. On a network, there are 'ports'. These ports are used for connecting to the server. Even though they are more symbolic that anything now, this is what is used. Differeent ports have different responsiblilities. For instance, port 22 is used as the SSH port. SSH is how to remotely connect to a server. Another exampe is port 80 and 8008 are used for http connections.  
### Port Status
There are a few different types of statuses for a port. This statuses are practically representing the responding status of the port .
Click here to learn more about these. In general, you'll only see open, closed and filtered. https://nmap.org/book/man-port-scanning-basics.html
## Basic Commands 
The basis of nmap is scanning an IP address. For this project, we're going to start with ada.gonzaga.edu. This is what im going to use for the rest of the examples, if not later specified.  
To scan ada run
```
nmap ada.gonzaga.edu
```
This will give you open ports on the server, but that's about it.   
To scan a singluar port run
```
nmap ada.gonzaga.edu -p port#
```
For multiple ports run
```
nmap ada.gonzaga.edu -p port#1,port#2
```
Now, scan the site 51.84.185.35....  
Nothing comes up, right? Well, server have the ability to disallow ping responses. So, if this becomes an issue you can run:
```
nmap -Pn ada.gonzaga.edu
``` 
This will essentially run a test that is guarenteed to find the result of each port.  
Scanning for a version service 
```
nmap -sV ada.gonzaga.edu
```
This commands takes a while so please be patient.  
To do extremely verbose protocols, use the -A flag like 
```
nmap ada.gonzaga.edu -p 80 -A
```
This will give the user practically as much information as they could ever need about the web server.  

## Importance

This is an extremely important tool to understand, for hacking and just networking in general. Finding open ports can lead to easy access on a server. Further, all of these open ports could potentially be connected, stealing information from it. The namp tool tends to access information that a regular user wouldn't see, such as the robots.txt file.  
The flags up above are just the tip of the iceberg! Further, you can scan a whole subnet of domains and get way more spefific with what is going on in the scans, with different types of packets being sent and more. 

## Testing it 
See what you can find on the site I set up at TBD.  
Run all different types of scans and see what you can find. In particular, look for files that the owner would not want you to see. 

## SSH 
SSH stands for secure shell. SSH allows you to connect to a web server without physcially being on the machine. 
In order to do this, the command for ada is
```
ssh student@ada.gonzaga.edu
```
However, there are more advanced features than this... A person can have a key set up for the server, instead of having a password into it. The syntax for that is
```
ssh -i key_file.pem student@ada.gonzaga.edu
```
This will allow you to log into a server with a key. Note, AWS keys use a ubuntu@.... for ec2 instances. 

## Learning basic networking
Here's how I learned what I know about it:
Microsoft certification area: https://www.youtube.com/watch?v=t9TmvFvYfWw&list=PLAVVUE5_qTL0sujvs5pGySHl1pXuw1job 
Then, just googling things I did not know. 

## Website fun
TBD


##


