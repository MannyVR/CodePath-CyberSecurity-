**Week 9: LAB**
**Milestone 0: Networking Toolbox**
    Run ifconfig/ipconfig/ip and determine the name/id of your primary network interface
      eth1
    What is your primary interface's IP address? Is it different from your public IP? Why or why not?
      10.0.3.15 This is different from my public IP address. The reason is because this is a private IP address that is unique to my compuer
    What is the MAC address of your primary interface?
    08:00:27:a0:39:09
    Identify and understand your loopback interface
![image](https://user-images.githubusercontent.com/36680097/40812285-e20f9874-64e9-11e8-9140-056bc0d1b168.png)

  **Ping**
    What is the IP address of codepath.com?
      198.58.125.217
    What is the IP address of google.com?
      172.217.5.78
    Why would the IP address of google.com change between runs or from different locations?
      Google has different servers in different parts of the world.
      ![image](https://user-images.githubusercontent.com/36680097/40813258-b5596a26-64ee-11e8-90b1-c6148d5560f1.png)

   **nslookup**
     Does the domain returned from nslookup match? If not, why not?
      yes
![image](https://user-images.githubusercontent.com/36680097/40813312-fab5be12-64ee-11e8-98f3-8486ef1e9afe.png)

   **traceroute**
     How many of the hops are the same? What accounts for this?
     They both are the same.
     Which has more hops? What accounts for the difference?
     They are the same.
     ![image](https://user-images.githubusercontent.com/36680097/40813462-d917d9f6-64ef-11e8-9dcf-f691ddb1ecef.png)
     
   **telnet**
      What's one thing that makes telnet insecure?
      DOES NTO ENCYPT DATA
      Can you telnet to codepath.com? What port is open and why?
      ![image](https://user-images.githubusercontent.com/36680097/40813720-307ca69e-64f1-11e8-8c4e-0077e19464f0.png)
   
   **curl and wget**
    Which would you be more likely to use for interacting with a RESTful API from the command line?
        cURL
    Which support recursive downloading?
        wget
    Which are you more likely to find pre-installed on a Linux OS?
        wget
    What is the syntax for each for downloading a file to the current directory?
        wget [option]  
        curl [options]
 
   **ssh and scp**
    Why is key authentication preferred to passwords?
        SSH keys are far more complex and secure than passwords
    What is the syntax for copying a file from a local folder to a remote one?
        scp [[user@]host1:]file1 ... [[user@]host2:]file2
        more info can be found here. https://www.garron.me/en/articles/scp.html#syntax
**Milestone 1: Security-Flavored Net Tools**
    **NetCat**
        ![image](https://user-images.githubusercontent.com/36680097/40815072-cbe5465c-64f8-11e8-9c65-d7f213aee40b.png)
    **NMAP**
        Challenge1: Run nmap against you localhost IP to see all open ports
            ![image](https://user-images.githubusercontent.com/36680097/40815216-b1321cc6-64f9-11e8-8a5b-fd30d238d69c.png)
 **Milestone 2: Grabbing Packets with tcpdump**      
    How many requests to load the main codepath.com page?
        12
    What type of resource accounts for most of the requests?
        seq, win, ack flags
    Now try the same exercise with https://security.codepath.com. What differences do you see in the output? What accounts for           those differences?
    68. The differences are the amount of packets. Again there is a lot of seq and ack.
   
        
    


**Week 9 Honey Pot Analysis: Assigment**
**Which Honeypot(s) you deploy?**
Dionaea

**Any issues you encounterd**
The most difficult challenge that I encountered while working on this challenge was getting the UI to be accessible via the 
web browser. This took a very long time, however after analyzing the information I learned that the mistake that I was  
that I was not installing the honeypot on the server. That was a problem. I was attempting to install the honey pot on my 
main machine. 

**Summary:**
Honey Pots are very important and can be crucial to protect our infrustructures. By implementing honeypots we are able to analyze 
how attackers are scanning our network. It is very interesting because once you analyze some of the honeypots youll see that 
there are many bots that are communicating to your machine from around the world. This shows you the intricate dangers that lie
in the internet. 
By looking at the traffic which is listed below in Milestone 5, you can see that there were a lot of attacks coming from within the
U.S. However shortly after the HoneyPot was set up I started get many attacks from different countries such as  Russia and China!
This didnt take long. 
If you look below, you will be able to see the milestones.

**Unresolved questions?**
I would really like to learn more about creating more effective honeypots, It is a very powerful concept. I would like to know
how I can trace back hackers. This is something I will be researching more.

**Milestone 0: To the Cloud**
![milestone0](https://user-images.githubusercontent.com/36680097/40676508-c077835e-632f-11e8-8e36-5e9b03ee30af.png)

**Milestone 1: Create MHN Admin VM**
![milestone1](https://user-images.githubusercontent.com/36680097/40676657-3ce19ed4-6330-11e8-9d1f-c86745bcac87.gif)

**Milestone 2: Install the MHN Admin Application **
![milestone2](https://user-images.githubusercontent.com/36680097/40805241-7cb3ff22-64d2-11e8-86ea-2cb4e45f6297.png) 

**Milestone 3: Create MHN Honeypot VM**
![milestone3](https://user-images.githubusercontent.com/36680097/40805183-50dbdf32-64d2-11e8-9484-1c86a9c9c7b1.png)

**MileStone 4: Install the HoneyPot application**
![milestone4](https://user-images.githubusercontent.com/36680097/40805521-5ee65002-64d3-11e8-8796-f7c536cd14dd.png) 

**MileStone 5: Attack **
![milestone5](https://user-images.githubusercontent.com/36680097/40806064-38cc767e-64d5-11e8-981e-0627e507b97b.png)

