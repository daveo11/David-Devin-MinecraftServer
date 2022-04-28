# David-Devin-MinecraftServer

## Overview:
Minecraft server ran on verison 1.17.1 with "Core Protect" and "Player Warps" plugins, capable of being ran locally, dockerized, or through an AWS EC2 instance.


## Running minecraft server locally:
1. run "cd server-data"
2. run "java -Xms1G -Xmx1G -jar paper-1.17.1-411.jar nogui" to start server


## Running minecraft server using docker:
1. Open docker desktop to confirm it is running
2. run "cd legacyserver"
3. run "docker-compose up" to build your server

## To close docker:
1. Use Ctrl + C in terminal
2. Then use "docker-compose down"


## Running minecraft server using AWS:
1. Create a t2.large EC2 instance using Amazon Linux 2 AMI 
2. Create a security group with the following specifications:
- SSH with port number 22 with source as anywhere
- Custom TCP with port number 25565 (minecraft specific) with source as anywhere
3. Create a new key pair to access EC2 instance
4. Select instance and connect to it using actions tab
5. Choose EC2 instance connect, and connect
6. run "sudo yum install java-17.0 -y" to update instance
7. run "sudo yum install java-17.0 -y" to install java
8. "wget https://launcher.mojang.com/v1/objects/c8f83c5655308435b3dcf03c06d9fe8740a77469/server.jar" (minecraft file installation)
9. "java -Xmx1024M -Xms1024M -jar server.jar nogui" to run minecraft server
10. "nano eula.txt" and change eula=false to eula=true


## Technologies used:

- [Docker](https://www.docker.com/)

- [AWS](https://aws.amazon.com/)

- [Paper](https://papermc.io/downloads)

- [Minecraft](https://www.minecraft.net/en-us)

## Background:

- [Docker-Minecraft help](https://www.youtube.com/watch?v=huDe-YSEVx4)

- [Minecraft Download](https://www.minecraft.net/en-us/download/server)

- [Local-Minecraft help](https://minecraft.fandom.com/wiki/Tutorials/Setting_up_a_server)



