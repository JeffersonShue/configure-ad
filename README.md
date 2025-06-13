![cloud2](https://github.com/user-attachments/assets/3a5c5567-549f-4146-9a0f-1911281f0d80)
<p align="center">



</p>

<h1>Creating a Windows (And Linux) Virtual Machine in the Cloud (Microsoft Azure)</h1>
In this walkthrough, we will create a Windows virtual machine (VM) in Azure. This skill set will be vital and is a key component to all of the IT projects listed. The same process applies when creating a linux virtual machine <br />

<h2>⚠️ Prerequisite</h2>

- <a href="https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account/search?ef_id=_k_Cj0KCQjwzYLABhD4ARIsALySuCTvMpKHbOeSo9lv81A8vCg1XGDNwpOIuOsD2o8pmLnyl7dVku-Yn3IaApK-EALw_wcB_k_&OCID=AIDcmmfq865whp_SEM__k_Cj0KCQjwzYLABhD4ARIsALySuCTvMpKHbOeSo9lv81A8vCg1XGDNwpOIuOsD2o8pmLnyl7dVku-Yn3IaApK-EALw_wcB_k_&gad_source=1&gbraid=0AAAAADcJh_uVoYZIZMJRJFQ3v8k-BGmp2&gclid=Cj0KCQjwzYLABhD4ARIsALySuCTvMpKHbOeSo9lv81A8vCg1XGDNwpOIuOsD2o8pmLnyl7dVku-Yn3IaApK-EALw_wcB)">Microsoft Azure account</a> 

<h2>💻 Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)

<h2>👨‍💻 Operating Systems Used </h2>

- macOS Sequoia
- Windows 10 Pro (21H2)
- Ubuntu Server 22.04

<h2>🪜 High-Level Steps</h2>

- Step 1: Create a Resource Group in Azure
- Step 2: Create the Windows VM in Azure
- Step 3: Create the Linux VM in Azure

<h2>Walkthrough Demonstration</h2>

<h3> Step 1: Create a Resource Group in Azure </h3>

<p>
<img width="750" alt="CVM RG1" src="https://github.com/user-attachments/assets/9a204856-d007-4472-a001-f53f870c86f5" />
</p>
<p>
- After creating an account with Microsoft Azure and getting logged in, you will end up at the Quickstart Center screen.
</p>
<br />

<p>
<img width="750" alt="CVM RG2" src="https://github.com/user-attachments/assets/be257212-9020-42f8-a04f-e7285de264dd" />
</p>

<p>
- Locate the Search Bar at the top of your screen. We will use this to find the Resource Groups. Select Resource Groups.
</p>

<br />

<p>
<img width="750" alt="CVM RG3" src="https://github.com/user-attachments/assets/0b5fc746-885f-48a5-a453-7893476f54bb" />
</p>

<p> - Since we do not have a resource group, Click the + Create button and let's get started!</p>
<br />
<br />

<p>
<img width="750" alt="CVM RG4" src="https://github.com/user-attachments/assets/9986ab58-999a-44b7-a807-85c9eef7b4e3" />
</p>

<p>
 
 1. The Subscription box should display whatever you chose when setting up your Azure account.  
 
 2. Name your resource group whatever you want, but make it something you can remember!
 
 3. Next, choose the Region. Now click next at the bottom of the screen.
</p>
<br />

<p>
<img width="750" alt="CVM RG5" src="https://github.com/user-attachments/assets/b6e9d80b-5dc8-4415-b4f1-6823dc5e1e36" />
</p>

<p>
- Review the Resource Group information and click Create. Make note of the name and region you used for future reference. 
</p>
<br />

<p>
<img width="750" alt="CVM RG6" src="https://github.com/user-attachments/assets/a1b7b6bd-c5f8-4af2-8a0c-07d8c762474d" />
</p>

<p>
- After clicking Create you will be directed back to the resource group section. You have successfully created your Resource Group in the Cloud. now let's create a virtual machine! </p>
<br />

<h3> Step 2: Create a Windows VM in Azure </h3><p>
<img width="750" alt="CVM 1" src="https://github.com/user-attachments/assets/b2df0ab8-de48-43bb-b35f-3e874a319e32" />
</p>

<p>
- From this screen, locate the search bar again and enter "virtual machines". Select "virtual machines", This will direct you to the Virtual Machines section.
</p>
<br />

<p>
<img width="750" alt="CVM 2" src="https://github.com/user-attachments/assets/67ff75e3-b5b2-4633-8e7c-8e4a696db477" />
</p>

- Select the first option, "Azure virtual machine" from the drop down and click + Create button.
</p>
<br />

<p>
<img width="750" alt="CVM 3" src="https://github.com/user-attachments/assets/73fbe4e8-4827-4a62-bfdf-c34cad139dea" />
</p>

<p>
<img width="750" alt="CVM 5" src="https://github.com/user-attachments/assets/4e088cf9-ac1a-4c64-b391-8904a566f2d2" />
</p>

<p>
 - Your subscription should already be selected.
 
 1. Choose the resource group we created earlier.
 
 2. Name the VM "windows-vm".
    
 3. Select the same Region as before. 
    
 4. Select "Windows 10 Pro, version 22H2" for the Image. This will be the Operating System (OS) for the VM. 

 5. Scroll down to select the Size. We want to use the "Standard_D2s_v5 - 2 vcpus, 8 GiB memory".
<p>- If you do not see this listed, click "See all sizes" to get more options. Sometimes the Region selected can cause this specific size to not appear. Just make sure the size you pick has at least 2 vcpus and 8 GiB memory. 
 
 6. Next, you will create a username and password for the VM. We will need this to log on later with a Remote Desktop Connection (RDP). *make sure you keep this information in a note.*</p>

 7. Now, locate the Licensing area towards the bottom of the screen. You will need to check the box to confirm. This is required because we are creating a Windows VM. Deployment will not work if left unchecked. Click "Next: Disks" to move on.

 8. We will leave the Disks settings at Default for what we are doing, but you can see all the differnet options Azure provides. Click "Next: Networking" to move on to Networking. This is where we will set the Vitrual Network for the VM.

 9.  Azure may auto populate a Network name for you. Go ahead and create a new one with a name of your choosing. Just note what you named the Network to refer back to later. We will need it for the Linux VM. You can leave the rest at Default setting. Azure will automatically assign the Subnet and Public IP for you. Leave the RDP Port as well. We will need access the VM via Remote Desktop Connection later. Click "Review + create" button.
</p>
<br />

<p>
<img width="750" alt="CVM 10" src="https://github.com/user-attachments/assets/83b3fcd4-391f-46a3-85f4-314b935a6cd0" />
</p>

<p>
 - Review all the informatiom for the Windows VM. Our Subsciption, RG, and Region are correct. We named the VM "windows-vm". The Image and Size are correct and we have RDP active. Simply click "Create".
</p>
<br />

<p>
<img width="750" alt="CVM 11" src="https://github.com/user-attachments/assets/c7b7029f-15cc-43b2-8264-c876a3d3a246" />
</p>

<p>
 - Once you click "Create", the Deployment of the Windows VM will begin. You will see "Your deployment is complete". Click "Create another VM" to get started on the Linux VM.
</p>
<br />

<h3> Step 3: Create a Linux VM in Azure </h3>

<p>
<img width="750" alt="CVM 12" src="https://github.com/user-attachments/assets/f2466234-fcbf-495d-a220-99eae0be07c8" />
</p>

<p>
Select the same RG that we created earlier. Name the VM "linux-vm" and choose the same Region as before. 
<br />

- Since this will be the Linux VM, select "Ubuntu Server 22.02" for the Image.

<p>- Choose the same Size option as before. "Standard_D2s_v5 - 2 vcpus, 8 GiB memory". </p>
<p>- Next, you will need to select "Password" for Authentication type. Azure defaults to SSH public key. Then, create a Username and Password. You can use information as the Windows VM to keep it simple.Once you are done, scroll done and click "Disks". Leave these options as default and skip to "Networking". 

- Make sure to select the same Virtual Network that we created earlier. We can leave everything else as default. Scroll down and click "Review + create".  

- On the next screen you will see the deployment of the Linux VM in progress.
  
- The Linux VM will be created. you can locate the search bar at the top of the screen and type in "virtual". Select "Virtual machines" and you will be direct to your newly created VMs.  
</p>

- You can view the Windows and Linux VMs we created in the Cloud. You will notice the RG and Locations match, what OS they are running, Public IP addresses, and so much more... </p>

</p>
<br />

<h2>Conclusion</h2>

<p>
This concludes our project. We sucessfully created a Resource Group, a Windows VM running Windows 10 Pro, and a Linux VM running Unbutu in the Cloud. Now, we essentially have three machines in total to use how we want for our IT needs. </p>
<p> You can see the many benefits that companies gain from using Cloud Services and Cloud Service Providers (CSP) without using terribly expensive hardware.  
</p>
<br />
