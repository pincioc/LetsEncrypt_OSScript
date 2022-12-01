# LetsEncrypt_OSScript

Create a new script named LetsEncrypt_OSSScript, copy the code and define a scheduler batch (in thi example every day):

/system scheduler
add interval=1d name=LetsEncrypt_OSScript_schedule on-event=Letsencrypt_OSScript policy=read,write,policy,test,sensitive

