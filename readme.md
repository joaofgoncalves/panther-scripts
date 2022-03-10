Disclaimer:

If you´re not sure what you do DON´T use this.

------------------------------------------------------------------------------------------------

# Increase the Panther X2 Peerbook:

You can use this script if you have access to the Hotspot via SSH

```
wget https://raw.githubusercontent.com/joaofgoncalves/panther-scripts/main/peerbook.sh -O - | sudo bash
```

To modify the docker.config file by hand (in case you want to change the parameters), use these steps

1) Go to file docker.config file directory:

```
cd //root/helium/overlay
```

2) Edit config file (needs admin permissions to write):

```
sudo vi docker.config
```

   2.1) Use mouse to position the cursor        

   2.2) Use [INSERT] key and enter the required values      

   2.3) To exit do [ESC] key and Ctrl + E and then write ```:wq!``` to save     
   
   2.4) Check the file with ```cat docker.config```      


3) Run the following command to update the peer list: 

```
sudo docker exec helium-miner miner peer book -c
```

4) Reboot the miner
