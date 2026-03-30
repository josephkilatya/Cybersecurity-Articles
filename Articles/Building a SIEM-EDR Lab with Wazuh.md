<!-- 

# Introduction


# Lab Setup
 Wazuh Virtual Machine: https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html
 Ubuntu 24.04.4 LTS: https://ubuntu.com/download/desktop
 Windows 10 Enterprise x64 ISO: https://go.microsoft.com/fwlink/p/?LinkID=2208844&clcid=0x409&culture=en-us&country=US
 VirtualBox: https://www.virtualbox.org/wiki/Downloads

 Ubuntu (Jammy Jelly Fish): https://releases.ubuntu.com/22.04/?_ga=2.149898549.2084151835.1707729318-1126754318.1683186906
 
 

## Creating a Virtual Network

Step 1: <img width="948" height="299" alt="image" src="https://github.com/user-attachments/assets/e5430adc-f839-4712-8f0b-80b66e5a560e" />

If you do not see the Network Section, You can Expand the Left Naviation bar by Clicking the **Menu** icon (3 bars) at the bottom left.
Pop up Windows: Do you want to allow this app to make changes to your devices. Click Yes.
New Interface: <img width="820" height="198" alt="image" src="https://github.com/user-attachments/assets/1ceb69c5-005c-4aad-b08d-c80b85fcf466" />
Right Click and Go to Properties. (Find Screenshot to Attach.)
COnfigure Adapter Manually. Go to DHCP Server.
<img width="823" height="404" alt="image" src="https://github.com/user-attachments/assets/fb290c71-14fb-4a2c-8f16-6636a774aeb4" />
Enable DHCP Server and Apply to save changes <img width="826" height="371" alt="image" src="https://github.com/user-attachments/assets/b6b76ddd-3e81-46d6-8b4c-48b0b707a0a3" />

Notice Adapter is enabled: <img width="828" height="145" alt="image" src="https://github.com/user-attachments/assets/bc187448-9b6d-40ad-b5d9-ef283a1b7240" />

Basics:
<img width="1007" height="770" alt="image" src="https://github.com/user-attachments/assets/eba0918b-62fd-4b4a-99fb-96c6c61e9392" />

<img width="1018" height="783" alt="image" src="https://github.com/user-attachments/assets/c0826eb2-8b56-4a8c-baed-2e718833db90" />

<img width="1033" height="770" alt="image" src="https://github.com/user-attachments/assets/b029043f-686b-4f4b-a0a8-812c5cf90b3c" />

<img width="868" height="624" alt="image" src="https://github.com/user-attachments/assets/6b67a56c-e2c8-4099-90f2-1438b8d741ef" />

Wait for Reboot


Skip email signup
Go for Domain Joined

<img width="997" height="600" alt="image" src="https://github.com/user-attachments/assets/3549f768-6182-4d69-b2e8-c197d73d2832" />

<img width="1005" height="623" alt="image" src="https://github.com/user-attachments/assets/3eda97cc-9982-498b-8943-63d16b61e880" />

Password -> Confirm Password

Security Questions

Wait

Privacy: Disable All
<img width="1021" height="734" alt="image" src="https://github.com/user-attachments/assets/979a35db-5c09-4290-afd2-dc24654b33f2" />

Cortana

<img width="1029" height="795" alt="image" src="https://github.com/user-attachments/assets/f6a42599-9ba9-42aa-a3b1-d72c51c77bb1" />



## Setting Up Windows VM
New -> <img width="876" height="256" alt="image" src="https://github.com/user-attachments/assets/e012086a-f34d-4fdd-b3ec-9b2a6dacd656" />

Skip: <img width="857" height="242" alt="image" src="https://github.com/user-attachments/assets/703e29c6-ecef-4615-a228-3e0877863ee3" />

<img width="878" height="165" alt="image" src="https://github.com/user-attachments/assets/5f936cd6-bf18-4bca-8b58-80ad546cb9ac" />

<img width="883" height="364" alt="image" src="https://github.com/user-attachments/assets/695b0036-7fbe-4956-8a77-c01621265394" />

Start Installation: <img width="952" height="313" alt="image" src="https://github.com/user-attachments/assets/5baac01e-59fc-48d6-8700-78a1ca69e2ee" />

<img width="631" height="468" alt="image" src="https://github.com/user-attachments/assets/3ace19b0-3038-49b4-9b78-0ab9622f635c" />

<img width="638" height="472" alt="image" src="https://github.com/user-attachments/assets/cff08bdf-a08e-4568-b918-fc894b772709" />

<img width="881" height="557" alt="image" src="https://github.com/user-attachments/assets/492b1104-71c4-4213-a989-38cfb5edc322" />

<img width="687" height="510" alt="image" src="https://github.com/user-attachments/assets/611cb040-6939-4fff-8d3c-74f5f8a78cfb" />

<img width="686" height="507" alt="image" src="https://github.com/user-attachments/assets/d4c541ca-c637-4352-930b-26884058c41e" />

<img width="689" height="515" alt="image" src="https://github.com/user-attachments/assets/65c6fe75-1e48-4fd8-a199-d284ea9d2092" />

<img width="710" height="527" alt="image" src="https://github.com/user-attachments/assets/67310e3c-2289-4d88-aff6-374cbf08e943" />

<img width="739" height="554" alt="image" src="https://github.com/user-attachments/assets/05c3f4eb-31fc-4355-888c-518e6155be58" />

<img width="1030" height="771" alt="image" src="https://github.com/user-attachments/assets/d3a54d83-ad82-4002-be95-45ae9be6e259" />

TAKE SNAPSHOT


DON NOT PUBLISH THIS:
While the idea is clever, the Windows Enterprise trial's license timer is designed to prevent this exact scenario. However, the built-in `slmgr /rearm` command is the legitimate way to extend your trial significantly.


<img width="893" height="284" alt="image" src="https://github.com/user-attachments/assets/e17da35b-210e-4ebc-a60a-14f9a2c0a24c" />



## Setting Up Linux VM
<img width="876" height="249" alt="image" src="https://github.com/user-attachments/assets/76938d9f-7ca9-46b0-9143-fd1ef1f0e736" />

<img width="874" height="268" alt="image" src="https://github.com/user-attachments/assets/de15e81d-eb22-4cc5-99e9-9bd4d1284d1a" />

<img width="870" height="167" alt="image" src="https://github.com/user-attachments/assets/80c1ddba-b49f-4407-95d7-22c26f01d3d8" />

<img width="878" height="420" alt="image" src="https://github.com/user-attachments/assets/0f770c83-43e6-4378-8f74-51d68841c5d5" />

<img width="1260" height="786" alt="image" src="https://github.com/user-attachments/assets/c93af960-9db2-4ec1-a490-92fe4498d779" /> Wait to finish

<img width="1266" height="785" alt="image" src="https://github.com/user-attachments/assets/d6c5fbbf-7a67-4534-bc3f-f2bdf8e80d07" />

<img width="573" height="221" alt="image" src="https://github.com/user-attachments/assets/503d72c0-8cb0-4c86-8a8d-5d1fefb374c3" />

<img width="1030" height="402" alt="image" src="https://github.com/user-attachments/assets/f87095bd-e5f1-4dec-9a2d-720d8abf7b0b" />

<img width="963" height="401" alt="image" src="https://github.com/user-attachments/assets/9694208d-bd43-415b-b233-5864505a8a58" />

<img width="1112" height="731" alt="image" src="https://github.com/user-attachments/assets/078f7124-7de3-400c-984b-b770ee705b19" />

<img width="1035" height="727" alt="image" src="https://github.com/user-attachments/assets/fd9b7b1e-eada-412b-ae7e-5b32051d878a" />

<img width="559" height="333" alt="image" src="https://github.com/user-attachments/assets/9f720c82-9d33-4fea-8b33-8f9dacd35179" />




Click New: <img width="784" height="556" alt="image" src="https://github.com/user-attachments/assets/d860b049-ad55-4198-a767-9701a434fbbc" />

Specifying virtual hardware:
<img width="627" height="162" alt="image" src="https://github.com/user-attachments/assets/782121cd-5864-40e5-931f-5211dfd97234" />

<img width="710" height="300" alt="image" src="https://github.com/user-attachments/assets/88ed6c8b-647c-4c53-8b57-8f1aa2e3b25b" />





Accessibilty in Ubuntu: Leave default
Select your keyboard layout
Connect to internet: Use wired connection
An update is available for the intaller: Update now or Skip
Hou would you like to install Ubuntu? Interactive installation
<img width="955" height="656" alt="image" src="https://github.com/user-attachments/assets/a645f9f8-ac81-472a-8fbb-cb4486002437" />
<img width="540" height="387" alt="image" src="https://github.com/user-attachments/assets/38b1060c-b8ec-4684-b1d9-33ca307ae154" />

Check ALl:
<img width="693" height="590" alt="image" src="https://github.com/user-attachments/assets/8a601c17-e710-4b29-adcb-5ca2005302bf" />

<img width="761" height="567" alt="image" src="https://github.com/user-attachments/assets/fc004314-3175-4b68-8b59-f727dd57cd34" />

<img width="560" height="498" alt="image" src="https://github.com/user-attachments/assets/85f2b7b1-60c5-4c24-a664-8899d52bdfaa" />


<img width="953" height="654" alt="image" src="https://github.com/user-attachments/assets/f106149a-3eb9-4ac2-b30f-f6823341bc0d" />

<img width="946" height="624" alt="image" src="https://github.com/user-attachments/assets/26c453d8-f242-427c-8a0d-0828ce3ee134" />

<img width="709" height="652" alt="image" src="https://github.com/user-attachments/assets/55baef24-6c7d-4b05-979b-93167a8d5f5d" />






## Setting Up Wazuh VirtualBox
Go to File -> Import Appliance -> Locate Wazuh Virtual Machine
<img width="589" height="253" alt="image" src="https://github.com/user-attachments/assets/cee03aeb-6b9a-40df-89e0-a26450a6c416" />
 Select VM and CLick Open:
 <img width="812" height="480" alt="image" src="https://github.com/user-attachments/assets/319aa5bc-8537-4832-98ba-57be6f8f5121" />

 Go to Settings -> MAC Address Policy -> Generate new MAC addresses for all network adapters: Leave the rest as default
 <img width="895" height="467" alt="image" src="https://github.com/user-attachments/assets/ee108115-12af-4820-a5e0-7cc7ce631995" />

 Go to Machines: You will find Imported Machine
 <img width="960" height="307" alt="image" src="https://github.com/user-attachments/assets/8e2050b1-0d64-4224-ac20-40669b595784" />

 ### Add VM to Virtal Network
 Select VM -> Go To Settings

 Reduce Memory: <img width="774" height="586" alt="image" src="https://github.com/user-attachments/assets/d2ea1801-8b7d-4521-9cb1-b6b4faf4730b" />

 Reduce Processor: <img width="590" height="294" alt="image" src="https://github.com/user-attachments/assets/93d0bc88-4fdb-431f-a4f2-af1cb27d2e4e" />

 To Be Continued






## Installing Agents (on Windows and Linux)

## Attack Simulation

## Logs Collection









Disk Size -> Finish
<img width="780" height="554" alt="image" src="https://github.com/user-attachments/assets/a7209b7e-c207-4bed-bb67-3fe2e97829f2" />

### Start Installation:
Select VM -> Start
<img width="838" height="296" alt="image" src="https://github.com/user-attachments/assets/47e4c0be-3525-476d-9453-d09aa7011bc9" />

<img width="721" height="484" alt="image" src="https://github.com/user-attachments/assets/3393b9a2-2352-4022-b23b-eb2658e5444f" />

Wait Ubuntu Preparation:

Select Language <img width="948" height="654" alt="image" src="https://github.com/user-attachments/assets/5ba1250a-d33c-47d7-9a88-6d0e55259742" />

-->


