# Vanilla-Minecraft

Basic Vanilla Minecraft

## Basic Vanilla Minecraft Setup

**// update software repositories**
$ `sudo apt update`

***// Install Firewall for Minecraft***
$ `sudo apt-get install ufw`

**// Configure required ports to be expossed**
$ `sudo ufw limit 22/tcp`
$ `sudo ufw allow 25565`

**// Global block (exception being the exposed ports)**
$ `sudo ufw default deny incoming`
$ `sudo ufw default allow outgoing`

**// Enable firewall**
$ `sudo ufw enable`

**// Verify firewall status**
$ `sudo ufw status`

**// find local ip of server**
$ `ip a | grep -i 192.168`

your ip is the first string of numbers with a /24 at the end of it
Example: 192.168.1.36

*remember the ip for later on*

**// install java**
*note: most modded minecraft servers run java8*

Install Java:
$ `sudo apt install openjdk-11-jre`

**// create a dedicated minecraft folder**

$ `mkdir minecraft`

$ `cd minecraft`

**// get the download link to the server files for vanilla minecraft**

https://www.minecraft.net/en-us/download/server

*copy the link of where to get the download (version may change in the future)*

"Download **minecraft_server.1.16.5.jar** and run it with the following command: "

**// download minecraft server files**

*paste the link you copied 1 space after wget*

$ `wget https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar`

**// initiate first setup**

*note: make sure to specify the correct name of your server file!*

(find the name of the file with the command: $ `ls`)

Run the start script for the server:
$ `java -Xmx1024M -Xms1024M -jar (server file name here) nogui`

**// accept minecraft eula**

$ `ls`

$ `nano eula.txt`

change the line `eula=false` to `eula=true`

To exit the file press

Ctrl+X then Y then Enter

**// run the start up script again**

(*This time start up with more ram allocated to the server*)

*note: make sure to specify the correct name of your server file!*

$`java -Xmx8096M -Xms8096M -jar (server file name here) nogui`

**// The world has generated**
once the world has generated join the server from the ip
exit the world and go back to the terminal and enter the command:
$ `stop`

**// Specify ip address of the server in server.properties**

$ `ls`
$ `nano server.properties`

find the line where it says `server-ip=` and insert your ip address after that

Example: `server-ip=192.168.1.36`

To exit the file press

Ctrl+X then Y then Enter

**// Start up server**
Now you can start up your server and play on your local network

$`java -Xmx8096M -Xms8096M -jar (server file name here) nogui`

To stop the server enter the command:
$ `stop`

**If you would like to play with friends port foward port 25565 on your
router**

$fin.$
