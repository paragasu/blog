---
layout: post
title: "Generate SSL certificates using letsencrypt" 
date: 2016-01-28 16:23:00 +0800    
categories: linux  
---

[Letsencrypt](https://letsencrypt.org) provide free ssl certificate. The only downside is that the certificate only valid   
for 3 months and then you have to renew the certificate again. 

    #git clone https://github.com/letsencrypt/letsencrypt
    #cd letsencrypt
    #./letsencrypt certonly --manual -d mydomain.com

On my debian server, The command will update packages and ask for root if you run as normal user
and it will require you to put some key file in the root domain for verification. 

    http://mydomain.com/.well-known/acme-challenge/random-key-filename


You have to make sure the content-type is text/plain for the verification to work.
The certificate will be available at /etc/letsencrypt.
The latest cert will be inside the /etc/letsencrypt/live folder. 


You need to update your server configuration to point to the cert file.


Related  
[Letsencrypt github](https://github.com/letsencrypt/letsencrypt)  
[Letsencrypt user guide](https://letsencrypt.readthedocs.org/en/latest/using.html#installation)


