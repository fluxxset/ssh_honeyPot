# Changing ssh Port 

- chage ssh port in file ( add any other than 22 )
 `sudo nano /etc/ssh/sshd_config`
- Update firewall rules for new port 
 `sudo ufw allow 1234/tcp`  or `sudo ufw allow OpenSSH`
- To apply the changes, restart the SSH service
 `To apply the changes, restart the SSH service`
- exit and login from new port 
 `ssh root@1.2.3.4 -p 1234`
 



if you dont have Digitalocean account use below link to create new onw and get 100$ free credit.
https://m.do.co/c/8f7b157b0fa2

<a href="https://www.digitalocean.com/?refcode=8f7b157b0fa2&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge"><img src="https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%201.svg" alt="DigitalOcean Referral Badge" /></a>
