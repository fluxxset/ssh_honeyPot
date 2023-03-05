# Changing ssh Port 

- Open a terminal or SSH client and log in as root or a user with sudo privileges.

- Edit the SSH daemon configuration file, usually located at /etc/ssh/sshd_config, using your preferred text editor. For example, you can use the nano editor with the command:
`sudo nano /etc/ssh/sshd_config`

- Find the line that specifies the SSH port number, which is usually set to Port 22. You can use the search function of your text editor to find it quickly.

- Change the port number to your desired value. For example, you can use Port 2222.

- Save the changes to the file and exit the text editor.

- Restart the SSH daemon to apply the changes. Depending on your Linux distribution, you can do this by running one of the following commands:
`sudo systemctl restart sshd`

- Optionally, configure your firewall to allow incoming connections on the new SSH port. For example, you can use the following command to allow traffic on port 2222 using the UFW firewall:

`sudo ufw allow 2222/tcp`

- That's it! You should now be able to connect to your Linux server using the new SSH port number. Note that you will need to specify the new port number in your SSH client configuration or command line, such as:

`ssh user@server -p 2222`



# Setting Up HoneyPot


-     Install the honeypot software

The honeypot software we'll use is called Cowrie. You can install it on your Linux server by running the following command:

`sudo apt-get update
sudo apt-get install cowrie`

-     Configure Cowrie

Once you've installed Cowrie, you'll need to configure it. The configuration file is located at /etc/cowrie/cowrie.cfg.

You can use the default configuration file, or you can customize it to your needs. Some things you might want to change include:

    The SSH port that Cowrie listens on (by default, it listens on port 2222)
    The log file locations
    The user and group that Cowrie runs as
    
-     Start Cowrie

To start Cowrie, run the following command:
`sudo service cowrie start`

-     Monitor Cowrie logs

Cowrie logs all SSH connections to your honeypot, along with the commands that are run. You can find the logs in the following locations:

    /var/log/cowrie/cowrie.log: This is the main log file, which logs all SSH connections and commands.
    /var/log/cowrie/tty/: This directory contains logs of each SSH session that connects to your honeypot.

You can monitor these logs to see if any SSH brute force attacks are being attempted on your server.

Note: Keep in mind that setting up a honeypot is not a foolproof solution and it's still important to implement security measures on your server to prevent attacks. Additionally, setting up a honeypot can potentially attract attackers to your server, so it's important to weigh the potential risks before implementing this solution.

if you dont have Digitalocean account use below link to create new onw and get 100$ free credit.
https://m.do.co/c/8f7b157b0fa2

<a href="https://www.digitalocean.com/?refcode=8f7b157b0fa2&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge"><img src="https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%201.svg" alt="DigitalOcean Referral Badge" /></a>
