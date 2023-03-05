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





