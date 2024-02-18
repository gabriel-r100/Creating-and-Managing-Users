<h1>Active Directory Lab - Uploading Content</h1>

![ActiveDirectoryLab drawio](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/23668c33-5348-408e-b41f-88ba144404ad)

<h2>Introduction</h2>

In this lab, I install Windows Server 2019 on a virtual machine using Oracle VirtualBox, configure an two network adapters, add Active Directory Domain Services, Router Services, and DHCP Services.<br>
Additionally, we generate users using a list of names (text file) and PowerShell and add them to an Organizational Unit named `_USERS`<br>
Lastly we ensure that an endpoint (Windows 10 VM) can join our Active Directory domain.




<h2>Windows Server 2019</h2>

![0-2-ActiveDirectoryLab drawio](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/90dc3da3-ee00-4d75-95ef-f96af14e622a)




<details><summary><h3>Virtual Machine Configuration</h3></summary>
  1. We start off by downloading a Windows Server 2019 ISO file from Microsoft. (Look for 'Windows Server 2019')
  2. When configuring the virtual machine, ensure to configure two network adapters, one will be set to NAT and the other to internal.
     a. NAT will be the internet facing one
     b. Internal will only be able to communicate with our virtual network
     c. Optionally, you can add more vCPUs and/or additional vRAM if you system can support it, otherwise default configurations are ok.

   ![4-1-ServerVM-Overview](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/7931229f-96ab-491f-b089-62d4812565f9)

  3. Once you have configured the settings, you can launch the virtual machine (VM) and continue through the installation process.
   ![5-Server2019-Installation](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/9905cd04-9e67-4012-9aa0-3a55dd1cb96d)

</details>




<details><summary><h3>Network Adapter Configuration and System Name</h3></summary>
  1. Now that we have successfully installed Windows Server 2019, we can configure and rename the network adapters for our use case.<br>
  2. Near the bottom right you will find the network settings icon, we select `Change adapter options`<br>
  3. We can find our two network interfaces here, we want to double click on them and select `Details`<br>
  
   ![7-Finding-NICs-VM-GUI](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/8de89c4c-3b24-43ee-9b55-28b2065efcf3)

  4. The one with a `IPv4 Address` that begins with 169 is our internal interface that we will rename `_INTERNAL`
  5. The second interface with will rename `_INTERNET`
   ![8-Renaming-Server-NICs](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/8b832026-f8be-4095-ae09-1f977eee7781)
  6. On our internal facing interface, we will select `Properties` and assign the static IP address of `172.16.0.1`. Because this server will server as a router for our virtual network, it does not require a value for gateway.
   ![9-Assigning-Static-IP-Info-Internal-NIC](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/a20d66e7-1d4a-4b8d-ae68-4d215a0d5118)

  7. Right-clicking on the start menu will bring up a menu, select `System` in here you can find the `Rename this PC` option to rename this host.
![10-1-Renaming-System](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/668ae43f-4b6a-4554-8c5c-9574b753aa90)
![10-2-Renaming-System](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/b4a38d36-fd2e-497c-969c-8c89655e2b22)

</details>




<h2>Server Roles and Features</h2>

![0-3-ActiveDirectoryLab drawio](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/0bc09da1-6d67-478d-9859-1aaf35a5fbce)




<details><summary><h3>Installing Active Directory Domain Services</h3></summary>
</details>

<details><summary><h3>Enabling Router Services</h3></summary>
</details>

<details><summary><h3>Adding DHCP Services</h3></summary>
</details>




<h2>Creating Active Directory Accounts Using PowerShell</h2>

![0-4-ActiveDirectoryLab drawio](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/09643b82-8a02-4bcc-8100-0ed8425b967c)





<h2>Connecting a Windows 10 Client to Our Domain</h2>

![0-5-ActiveDirectoryLab drawio](https://github.com/gabriel-r100/Active-Directory-Lab/assets/55646808/c54993e6-f66c-40a2-a5c0-bc4d19646eae)




<details><summary><h3>Virtual Machine Configuration</h3></summary>
</details>

<details><summary><h3>Renaming Endpoint and Joining Domain</h3></summary>
</details>
