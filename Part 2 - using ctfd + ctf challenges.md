Used https://github.com/mdulin2/SC4 to transfer CTF challenges from last year to prepare the Cybersecurity class in competing in Cyber Cup 2024

![files](https://github.com/crazycoderLucy/cvnetworking23-24/assets/117693275/186e1046-3a97-4844-a95b-b990debde3fc)


1. Installed the CTFd through the terminal using "wget"

2. The docker container that we started to get the webGUI portion working, had kept crashing. Looking into as why it was crashing, it was because we had another Docker container running on the same port, which can cause a lot of issues in general.

3. We couldn't start the Nginx webserver due to it not being installed. We had came to this conclusion when the docker container was giving us a error of not being able to find the Nginx webserver. Once we had gotten Nginx installed, the docker container started up with no issues at all.

4. Edited the CTFd to make sure everything looked proper. Doing this, we also decided to change the permissions so the players couldn't access the admin features, we created the administrator accounts and changed how the CTF platform looks. 
  
5. Decided on flag syntax, sent out CTF challenge assignments 
    1. Decided to use Cyber Cup Challenges on top of the planned CTFs
    2. Made a couple of our own
6. Configured docker to run on start
    1. Used command that runs docker into a bash script to reference in crontab
7. Troubleshooting Cats Challenge:
    1. Port is already allocated for cats web page - We had to change the port mappings for the cat challenge since it would cause issues with the other docker containers that were already running. 
    2. Configure challenge to run when link is clicked - When you're looking at through the challenge details, we had  sure the challenge to auto-run when we clicked on the link so we aren't using unneccesary resources that could be allocated to something else. We had to change the ports for each challenge so there was no conflict with the other challenges that would be running. 
8. Setting up Cloudflare ARGO tunnel
    1. We had dismissesd setting up the Argo tunnel for a few reasons. We had realized we don't want this to be publicily accessible from the outside network. We also came to the conclusion that our network infastructure would be incompatible with using Argo due to filtering and core services that Cloudflare needs in order for Argo to work. 
9. Trevor bought a domain
    1. I thought this would be a good idea since trying to memorize a IP address would be more difficult than trying to remember a IP address. We scrapped using the domain since we had realized we would have to change the hosts files on the clients Windows machines. Manually changing the hosts file would've taken some time to do and since any changes we make towards the clients machine, gets reverted after the machine reboots.
10. Internal Server
    1. Decided to switch over to just using ip address



Reflection:
Overall, we learned how to setup a webserver, severel Docker containers, learn several troubleshooting steps, and learned about how Cloudflare services function. Installing Nginx on a Ubuntu environment can be quite tricky if you don't know how to use the CLI within Linux. At first when we installed the docker service, we had came to the realization that we would have to use Docker-compose instead of the normal Docker that gets installed. We figured Docker-compose would be better since you can run all of the challenges at once through a single .yaml file (which if you didn't know, .yaml is the preferred docker-compose file type and can give you a lot more to configure.) The troubleshooting steps that we had to take were quite extensive. This took a lot longer than it should've due to fixing one issue would break another couple "working" containers. **I will finish the rest of edits later today/tonight**
