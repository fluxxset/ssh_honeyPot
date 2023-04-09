# Changing ssh Port 

- chage ssh port in file ( add any other than 22 )
 `sudo nano /etc/ssh/sshd_config`
- Update firewall rules for new port 
 `sudo ufw allow 1234/tcp`  or `sudo ufw allow OpenSSH`
- To apply the changes, restart the SSH service
 `To apply the changes, restart the SSH service`
- exit and login from new port 
 `ssh root@1.2.3.4 -p 1234`
 
 
 # Setting UP Honeypot

- download honeypot script from github
`curl https://raw.githubusercontent.com/fluxx03/ssh_honeyPot/main/honeypot.py -o honeypot.py`
- running script 
`python3  honeypot.py`
to run in background 
`nohup python3  honeypot.py >> out.txt &`




if you dont have Vultr account use below link to create new onw and get 100$ free credit.
[https://m.do.co/c/8f7b157b0fa2](https://www.vultr.com/?ref=9418944)

<a href="https://www.vultr.com/?ref=9418944"><img src="https://www.vultr.com/media/logo_mono_ondark.png?_gl=1*c52ya5*_ga*NzE2NTMyMTc2LjE2ODA2MTQzMzc.*_ga_K6536FHN4D*MTY4MTA1OTkyMC4yOC4xLjE2ODEwNjA4MjYuNTkuMC4w" alt="Vultr Referral Badge" /></a>
