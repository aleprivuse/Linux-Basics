# Networking 101

it would be greate if you completed The port file first

## Firewall

Now what is a firewall you ask you can think it like a bouncer on a club its blocks peaplo form entering thats a firewall. you can use this command to see if you Firewall is active

### commads 

1. sudo ufw(stands for uncomplicated Firewall) status = see the of your firewall
2. sudp ufw enable = enable the firewall 
3. sudo ufw disable = disable the firewall

note : always enable the SSH first so you dont lock out yourself form your own server whit this command
 sudo ufw allow 22 = allow the port of SSH

4. sudo ufw allow 22 = open an port and allow it
5. sudo ufw deny from (IP) = Ip ban
6. sudo ufw allow from (IP) to any port 22 = allow the ip to come in to any of the port 22


 
