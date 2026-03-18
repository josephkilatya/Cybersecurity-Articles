# Introduction


# Lab Setup
 Wazuh Virtual Machine: https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html
 Ubuntu 24.04.4 LTS: https://ubuntu.com/download/desktop
 Windows 10 Enterprise x64 ISO: https://go.microsoft.com/fwlink/p/?LinkID=2208844&clcid=0x409&culture=en-us&country=US
 VirtualBox: https://www.virtualbox.org/wiki/Downloads
 
 

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








## Setting Up Windows VM

## Setting Up Linux VM
Click New: <img width="784" height="556" alt="image" src="https://github.com/user-attachments/assets/d860b049-ad55-4198-a767-9701a434fbbc" />

Specifying virtual hardware:
<img width="627" height="162" alt="image" src="https://github.com/user-attachments/assets/782121cd-5864-40e5-931f-5211dfd97234" />


Disk Size -> Finish
<img width="780" height="554" alt="image" src="https://github.com/user-attachments/assets/a7209b7e-c207-4bed-bb67-3fe2e97829f2" />

### Start Installation:
Select VM -> Start
<img width="838" height="296" alt="image" src="https://github.com/user-attachments/assets/47e4c0be-3525-476d-9453-d09aa7011bc9" />

<img width="721" height="484" alt="image" src="https://github.com/user-attachments/assets/3393b9a2-2352-4022-b23b-eb2658e5444f" />

Wait Ubuntu Preparation:





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


