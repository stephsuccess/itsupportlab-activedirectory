[README.md](https://github.com/user-attachments/files/27150476/README.md)
# How to Setup a Basic Home Lab Running Active Directory (Oracle VirtualBox) | Add Users w/PowerShell

This is a step by step guide on how to set up an Active Directoy home lab based on the training by Josh Madakor. 

## Diagram
![Diagram](active_directory_diagram.jpg)

## Download and install Oracle VirtualBox from the official website.
[Oracle Virtual Box](https://www.virtualbox.org/)

## Download the Windows 10 and Server 2019 ISO files.
[Windows 10 iso](https://www.microsoft.com/en-us/software-download/windows10ISO)
[Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)

## Create a new virtual machine by clicking on "New" in VirtualBox, naming it "Domain Controller," and selecting the "Windows Server 2019" ISO file as the boot media.

<img width="659" height="579" alt="Pasted image 20230402145533" src="https://github.com/user-attachments/assets/88e32e79-2a78-48f9-ac4c-dfd17fd4afd0" />


<img width="598" height="542" alt="Pasted image 20230402145610" src="https://github.com/user-attachments/assets/98973513-446d-4d32-bbcc-42b3e139a1d7" />


##  Configure the virtual machine by giving it two network adapters: one for connecting to the internet and the other for the private network.

<img width="695" height="578" alt="Pasted image 20230402145806" src="https://github.com/user-attachments/assets/ddbd2391-0fae-46d2-a86e-f9e931c5a0ec" />


<img width="696" height="576" alt="Pasted image 20230402145820" src="https://github.com/user-attachments/assets/2654cf73-5346-4c19-bc31-30a65ecb4dea" />


##  Install Server 2019 on the virtual machine and assign IP addressing for the internal network.

<img width="638" height="267" alt="Pasted image 20230402150458" src="https://github.com/user-attachments/assets/ff2ca736-f556-4ba8-a847-9dcaa80f7fe2" />


<img width="396" height="454" alt="Pasted image 20230402150538" src="https://github.com/user-attachments/assets/e985d611-fdb8-4bf8-af42-ade76e37e49a" />

##  Name the server and install Active Directory to create the domain.

<img width="784" height="562" alt="Pasted image 20230402150727" src="https://github.com/user-attachments/assets/b9f8c2a7-dba9-4312-99cb-2a93a0b4e01f" />

<img width="1350" height="774" alt="Pasted image 20230402153253" src="https://github.com/user-attachments/assets/2b4f1616-a508-4238-aa97-40fd5c6ac326" />


##  Configure routing so that clients on the private network can access the internet through the domain controller.
<img width="618" height="444" alt="Pasted image 20230402154123" src="https://github.com/user-attachments/assets/df569b53-f822-4655-8f38-be2caa70776d" />

<img width="787" height="557" alt="Pasted image 20230402153904" src="https://github.com/user-attachments/assets/095d277f-78f2-4f03-bfea-636eaafdef96" />

<img width="1496" height="755" alt="Pasted image 20230402153829" src="https://github.com/user-attachments/assets/99913c9a-c93a-4558-a8f1-c42f9e00d998" />


##  Set up DHCP on the domain controller.
![](attachments/Pasted%20image%2020230402154312.png)

![](attachments/Pasted%20image%2020230402154041.png)

![](attachments/Pasted%20image%2020230402154439.png)


##  Run the PowerShell script to create 1000 users in Active Directory.

[Power Shell script for creating users](https://github.com/joshmadakor1/AD_PS)

##  Create a new virtual machine named "Client1" and install Windows 10 on it.

![](attachments/Pasted%20image%2020230402155056.png)


##  Connect the client machine to the private network and join it to the domain.

![](attachments/Pasted%20image%2020230402155713.png)

![](attachments/Pasted%20image%2020230402155807.png)

##  Log into the client machine with a domain account.

![](attachments/Pasted%20image%2020230402160005.png)

![](attachments/Pasted%20image%2020230402160120.png)
