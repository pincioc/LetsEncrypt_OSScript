# Mikrotik LetsEncrypt_OSScript
This script automates the generation and renew of certificate provide by Let's Encrypt on Mikrotik devices.

Requirements:
 - RouterOS v.7
 - Public IP on WAN Interface or port 80 forward 


Create a new script named LetsEncrypt_OSScript, copy the code form LetsEncrypt_OSScript.txt file and define a scheduler batch (in this example every day at 02:00 AM):

/system scheduler add interval=1d name=LetsEncrypt_OSScript_schedule on-event=LetsEncrypt_OSScript policy=read,write,policy,test,sensitive start-time=02:00:00

If you don't want use the CloudIP hostname ( xxx.sn.mynetname.net) you can uncomment the 4th line and set the FQDN

Be carefull on Let's Encrypt Rate Limits in your tests https://letsencrypt.org/docs/rate-limits/