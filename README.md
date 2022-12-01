# Mikrotik LetsEncrypt_OSScript
This script automates the generation and renew of certificate provide by Let's Encrypt on Mikrotik device

Requirement:
 - RouterOS v.7
 - Public IP on WAN Interface or port 80 forward 


Create a new script named LetsEncrypt_OSScript, copy the code form LetsEncrypt_OSScript.txt file and define a scheduler batch (in thi example every day):

/system scheduler add interval=1d name=LetsEncrypt_OSScript_schedule on-event=Letsencrypt_OSScript policy=read,write,policy,test,sensitive

If you don't want use the CloudIP hostname ( xxx.sn.mynetname.net) you can uncomment the 4th line and set the FQDN