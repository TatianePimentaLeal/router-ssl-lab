# CREATING A LOCAL CERTIFICATE - ROUTER SSL LAB

## Objective

Understand the aim of a certification by showing how simple it is to create and use a security certificate, and implement it in a server to encrypt all the information.

### Skills Learned

- Create a local security certification.
- Implement a security certification in a server.
- Proficiency in analyzing the impact of a configured HTTPS in a website.
- Development knowledge regarding router configuration tools.

### Tools Used

- Mikrotik Cloud Hosted Router VDI image version 6.49.17 stable as a hard disk.
- WinBox from Mikrotic website to upgrading RouterOS and make the needed adjustments.
- VirtualBox to create a VM lab.

## Steps





To access Mikrotik website, and go for “Cloud Hosted Router” to download “VDI Image”

*Ref 1: Mikrotic downloads page*





Configurate your VM as informed in the image

*Ref 2: VM Creation*





Select "VirtualBox Host-Only Ethernet Adapter"

*Ref 3: VM Configuration*



By default the user is "Admin" and there is no password

*Ref 4: Router Login 1 *





At the software license, choose "n" for no and create a password of your own

*Ref 5: Router Login 2*





In the access screen we can see we could access, but it is still not secured

*Ref  6: Access test*



Download the Winbox at the "Upgrading RouterOS" page

*Ref 7: Winbox install*



Then configure it according to the images below:



*Ref 8: Winbox Configuration*



*Ref  9: Winbox Configuration*



*Ref 10: SSL*





When try access the page again, it will show this screen, as it does not contain a certificate yet

*Ref 11: Certificate none*



Comebak to the admin from Mikrotic to provide the proper adjustments, according to the following screens:



*Ref 12: Certificate none adjustments*



*Ref 13: Certificate none adjustments*



As we will not use a DNS now, in "Common Name" put the IP Address, and inform what the certificate will do.

*Ref 14: Certificate none adjustments*



*Ref 15: Certificate none adjustments*



Here you should select "Sign" before click on Apply

*Ref 16: Certificate none adjustments*



But adjusting it, the "LocalCA" will be registered and it will be possible to proceed with the sign select and move on for the next steps

*Ref 17: Certificate none adjustments*





It will be correct, as it is possible to see

*Ref 18: Certificate none adjustments*





Now we will have a certified entity created and generated in the server.

It is needed to assign the certification in the browser. 

Now it is possible to create a browser certificator:



*Ref 19: Certificate none adjustments*



The new certificat3e create, the certified entity, is the first certificate "LocalCA". To the purpose of this case study, we will use it:



*Ref 20: Certificate none adjustments*





With a double click in the "none" from SSL, it will be possible to include the www website certificate 

*Ref 21: Certificate none adjustments*



It will appears according to the image.

So, once you try to access the website again, it will appear with a HTTPS:



*Ref 22: Certificate HTTPS active*



And it will be done

*Ref 23: Router Access HTTPS*


