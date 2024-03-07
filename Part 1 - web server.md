**Preliminary Steps:**
- Organized PC Layout
- Installed 4 SSDs

**Windows Server:**
- Installed Windows Server 2022
- Configured Raid 1+0 on Windows Server
- Used Windows Server “Add Roles and Features” Wizard to configure
- Containers and Windows Subsystem for Linux
- Downloading Docker Desktop
- Downloading WSL -> troubleshooting, not downloading properly
- Remove Windows Server and change it to Ubuntu - starting over

**Project Process:**
We first started out using Windows Server as the host operating system but we decided to switch to Ubuntu to make things simpler. 

**LINUX:**
- Download Docker
- Download ctf platform
- Killed the first docker container and started building the CTFd docker container through CLI
- Configured cisco switch (no switch security settings yet)
    - Username: ctfadmin
    - Password: J0e-P@u!e7!
- Removed the router due to issues with double NAT
- Although we wanted to build a parity drive, it didn’t happen
- If RAID fails, parity drive rebuilds the failed drive
- Download mdadm (administration tools for RAID)
- Create RAID device
- Started docker container from repository

![starting](https://github.com/crazycoderLucy/cvnetworking23-24/assets/117693275/3f7341e0-2eea-48d2-986e-b38e95fa2964)

- Test connection worked as expected through IP address and port 8000

![ipaddress](https://github.com/crazycoderLucy/cvnetworking23-24/assets/117693275/3126052c-1e2c-412b-be30-2a1dd81a5d57)

