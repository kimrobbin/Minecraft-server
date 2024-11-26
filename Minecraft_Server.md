# Vanilla Minecraft server For newest version

Fyi: To get the link to use wget you have to righ-click on the lick on the site and click copy link

<img src="link.jpeg" height="200px"/>

<br>

```sh
   # Download Open jdk (java)
   sudo apt install openjdk-17-jdk

   # Now go to this site and download the minecraft_server or use the script to download the server file. 
   https://www.minecraft.net/en-us/download/server 
   
   <br> wget https://piston-data.mojang.com/v1/objects/45810d238246d90e811d896f87b14695b7fb6839/server.jar
   
   # Now make a folder on your desktop or where you want it
   mkdir "name"

      # Move the server.jar file to desktop(or where you have the folder) then into the folder  
      mv server.jar "path"


   # In the server folder run the follwing command
   java -jar server.jar    # The command made all the files needed 

   
      # Now change the eula from false to true 
      nano eula .txt

   # Create the config file that makes you bale to change ram config
   nano start.sh

      # Now past this command(the hastage underneat is part of the script):
      
      #!/bin/sh
      java -Xms2094M -Xmx6144M -jar server.jar # You change the -Xms and -Xmx to configure min- maximum ram
                                                     # Now click crt-O to save and crt-X to exit

   # You should then be back in terminal. to run the file, you have to mark the file as an executable. 
   sudo chmod +x start.sh

   # And now to start the server 
   sudo ./start.sh

   # Now at last open the port that minecraft is using 
   sudo ufw allow 25565

   # If you want to top the server type stop in the consoll 
```

# Modded Minecraft server

<br>

   Fyi:

 <img src="forgeskip.jpeg" height="auto"  />
   This is how to get forge. More detailes in step 3.
   <br>
   To get forge go to https://files.minecraftforge.net/net/minecraftforge/forge/ Or type forge in the browser
   <br>
   I sugest you get your mods from curseforge

<br>

```sh
   # Make sure you have java installed (jdk) if not run this command 
   sudo apt install openjdk-17-jdk

   # Now you have to find out witch version of forge you need. i will use 1.20.1 in this Tutorial 
   wget https://maven.minecraftforge.net/net/minecraftforge/forge/1.20.1-47.3.0/forge-1.20.1-47.3.0-installer.jar
      # To get the link you have to first click on the installer and then get the link from the skip button

   # When you have your file run this command
   java -jar "Filename/forgefile" --installServer
   # Now way untill the download is done

   #If you want to change the magimum ram use this command and then change the -Xmx4G to your desired max ram 
   nano user_jvm_args.txt
   
   # Now we are almost done, but we need to start the server for the first time and accept eula 
   ./run.sh # This starts the server 
   nano eula # This allows us to change the eula to true

   # If you type "ls" now you will see a mod folder, move into it and put your mods here. There are multiple ways to download mod and here is a exemple.
   wget https://mediafilez.forgecdn.net/files/5393/334/ZZ.JJThunder_To_The_Max_1.20.1_v0.2.0.jar # If you need help to get the link follow the video bellow 


   # Now all you need to do is start the server
   ./run.sh

   # If you want to change the configs of the server
   nano server.properties

   # if you want to give yourself operator/op 
   op "minecraft name"


```

  Wget forge mods tutorial: <br>
   <a href="https://udeoslokommuneno-my.sharepoint.com/:v:/g/personal/kifoa001_osloskolen_no/EVFQx33T5uBMj3wPrJbWTEUBbOgtj-JF_z2Ko0t4wBxVrw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=e0sRy0"> <img src="curse.jpeg" height="200px">  </a>