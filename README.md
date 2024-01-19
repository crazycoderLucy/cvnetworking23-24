# cvnetworking23-24
semester final

[Updated 1/16] Networking Project
By: Trevor, Will, Kyler, Lucy [TWKL]
Preface:
This is NOT a step-to-step tutorial but rather documents our thought process, changes, problems, and failures that we have encountered when working on this project. 

We used the computer that was previously used for Virtual Reality gaming, and transformed it into a CTF server with:
- An Ubuntu Server operating system
- RAID 10 for redundant CTF storage
- Docker

Why this project:
The overall arching goal of this project is to understand how to build a web server

Primary Materials: 
- Cisco Business CBS350-8T-E-2G Managed Switch - amazon
- 4 SSD’s -  crucial	
- Usb to Ethernet Console Cable x3 - amazon
- More Mounting Brackets
- Coursera PC
- More drives to make it a server
- More RAM
- CTF platform: host on our server + make new challenges

References:
- https://www.baeldung.com/linux/raid-intro
- https://www.digitalocean.com/community/tutorials/how-to-create-raid-arrays-with-mdadm-on-ubuntu-22-04
- https://medium.com/csictf/self-hosting-a-ctf-platform-ctfd-90f3f1611587

Project Plan
Using the materials, we will set up the server
Figure out the OS - on Linux
When hosting the CTF platform
Consider multipurpose uses (file shares)
Help from Mr. Steiner, etc.
Use cybercup github repo
Post on LinkedIn the final result

Project Process
Organized PC Layout
Installed 4 SSDs
Installed Windows Server 2022
Configured Raid 1+0 on Windows Server
In Windows Server “Add Roles and Features” Wizard
Containers and Windows Subsystem for Linux
Downloading Docker Desktop
Downloading WSL -> troubleshooting, not downloading properly
Remove Windows Server and change it to Ubuntu - starting over


LINUX
Download Docker
download ctf platform
killed process and started building docker through CLI
configuring cisco switch
remove router -> double NAT is unnecessary (router got hit with banhammer)
 want to build parity drive 
 Download mdatdm
create RAID device
started docker container from repo
Install CTFd
Docker-compose stopped unexpectedly
Cannot start nginx, install nginx -> error addressing 
Port is already allocated for cats web page
Absurdly productive amount of time spent configuring essential aspects of the ctfd
Create admin accounts for all project contributors
setting up cloudflare argo tunnel 
Cloudflare argo no worky because school internet doesn’t like tunnels
Trevor willingly purchased a domain for this project - spashaben.com
Decided on flag syntax, sent out CTF challenge assignments 
