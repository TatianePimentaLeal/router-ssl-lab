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

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref1.Mikrotik-Downloads.png)

To access Mikrotik website, and go for “Cloud Hosted Router” to download “VDI Image”

*Ref 1: Mikrotic downloads page*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref2.VM-Creation.png)

Configurate your VM as informed in the image

*Ref 2: VM Creation*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref3.VM-Config.png)

Select "VirtualBox Host-Only Ethernet Adapter"

*Ref 3: VM Configuration*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref4.Router-login1.png)

By default the user is "Admin" and there is no password

*Ref 4: Router Login 1 *



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref5.Router-login2.png)

At the software license, choose "n" for no and create a password of your own

*Ref 5: Router Login 2*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref6.Access-Test.png)

In the access screen we can see we could access, but it is still not secured

*Ref  6: Access test



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref7.Winbox.png)

Download the Winbox at the "Upgrading RouterOS" page

*Ref 7: Winbox install*



Then configure it according to the images below:

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref8.Winbox-Config1.png)

*Ref 8: Winbox Configuration*

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref9.Winbox-Config2.png)

*Ref  9: Winbox Configuration*

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref10.SSL-443.png)

*Ref 10: SSL*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref11.Certificate-none.png)

When try access the page again, it will show this screen, as it does not contain a certificate yet

*Ref 11: Certificate none*





Comebak to the admin from Mikrotic to provide the proper adjustments, according to the following screens:

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref12.Certificate-none-adjustment1.png)

*Ref 12: Certificate none adjustments*

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref13.Certificate-none-adjustment2.png)

*Ref 13: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref14.Certificate-none-adjustment3.png)

As we will not use a DNS now, in "Common Name" put the IP Address, and inform what the certificate will do.

*Ref 14: Certificate none adjustments*

![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref15.Certificate-none-adjustment4.png)

*Ref 15: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref16.Certificate-none-adjustment5.png)

Here you should select "Sign" before click on Apply

*Ref 16: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref17.Certificate-none-adjustment6.png)

But adjusting it, the "LocalCA" will be registered and it will be possible to proceed with the sign select and move on for the next steps

*Ref 17: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref18.Certificate-none-adjustment8.png)

It will be correct, as it is possible to see

*Ref 18: Certificate none adjustments*





Now we will have a certified entity created and generated in the server.

It is needed to assign the certification in the browser. 



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref19.Certificate-none-adjustment9.png)

Now it is possible to create a browser certificator:

*Ref 19: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref20.Certificate-none-adjustment10.png)

The new certificat3e create, the certified entity, is the first certificate "LocalCA". To the purpose of this case study, we will use it:

*Ref 20: Certificate none adjustments*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref21.Certificate-none-adjustment11.png)

With a double click in the "none" from SSL, it will be possible to include the www website certificate 

*Ref 21: Certificate none adjustments*





It will appears according to the image.



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref22.Certificate-HTTPS.png)

So, once you try to access the website again, it will appear with a HTTPS:

*Ref 22: Certificate HTTPS active*



![alt text](https://github.com/TatianePimentaLeal/router-ssl-lab/blob/main/Router-SSL-Lab_Project_Cybersecurity_imgs/Ref23.Router-Access-HTTPS.png)

And it will be done

*Ref 23: Router Access HTTPS*
