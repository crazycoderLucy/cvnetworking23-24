**Preliminary:**
Organized PC Layout
Installed 4 SSDs

**Windows Server:**
Installed Windows Server 2022
Configured Raid 1+0 on Windows Server
In Windows Server “Add Roles and Features” Wizard
Containers and Windows Subsystem for Linux
Downloading Docker Desktop
Downloading WSL -> troubleshooting, not downloading properly
Remove Windows Server and change it to Ubuntu - starting over

**Project Process:**
We first started out using Windows Server as the host operating system but we decided to switch to Ubuntu to make things simpler. 

**LINUX:**
Download Docker
Download ctf platform
Killed the first docker container and started building the CTFd docker container through CLI
Configured cisco switch (no switch security settings yet)
Username: ctfadmin
Password: J0e-P@u!e7!
Removed the router due to issues with double NAT
Although we wanted to build a parity drive, it didn’t happen
If RAID fails, parity drive rebuilds the failed drive
Download mdadm (administration tools for RAID)
Create RAID device
Started docker container from repository
Test connection worked as expected!

