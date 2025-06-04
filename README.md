![cloud2](https://github.com/user-attachments/assets/bfb02120-7283-49b3-850a-5f6497fbd5e9)
<p align="center">
 
</p>

<h1>Creating a Windows and Linux Virtual Machine in the Cloud (Microsoft Azure)</h1>
In this walkthrough, we will create a Windows and Linux virtual machine (VM) in Azure. This skill set will be vital and is a key component to all of the IT projects listed. <br />

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
<img width="750" alt="CVM RG1" src="https://github.com/user-attachments/assets/1c6e64ad-18da-497c-8ccc-3fe556fd6325" />
</p>
<p>
- After creating an account with Microsoft Azure and getting logged in, you will end up at the Quickstart Center screen. Welcome to Azure!
</p>
<br />

<p>
<img width="750" alt="CVM RG2" src="https://github.com/user-attachments/assets/225c4871-81f4-4c60-8cd1-f60c93de7d8c" />
</p>
<p>
- Locate the Search Bar at the top of your screen. We will use this to find the Resourse Groups. Notice the options that populate as you type "resource" into the search bar. Select Resource Groups.
</p>

<br />

<p>
<img width="750" alt="CVM RG3" src="https://github.com/user-attachments/assets/72a12b56-b80c-4cd8-85ea-20661e028bd0" />
</p>
<p> - Oops! The resource groups seem to be missing... Have no fear, IT is here! 😎 Click the + Create button and let's get this party started!</p>
<br />
<br />

<p>
<img width="750" alt="CVM RG4" src="https://github.com/user-attachments/assets/f1b182f0-e9db-475e-9036-6241d4c9366e" />
</p>
<p>
 
 1. The Subscription box should reflect whatever you chose when setting up your Azure account. If you do not see that, click the drop down arrow to find it. 
 
 2. Now, name your Resource Group (RG). This RG is where our VMs will be stored in the Cloud.
 
 3. Next, choose the Region. *Pro Tip: Select (US) East US 2 for ALL Region options. Making sure the Region matches for eveything we create will save you from future headaches.* Now click next at the bottom of the screen.
</p>
<br />

<p>
<img width="750" alt="CVM RG5" src="https://github.com/user-attachments/assets/4d913c40-61ef-4e03-8488-d6ab4bb06540" />
</p>
<p>
- Review the Resource Group information and click Create. Make note of the name and region you used for future reference. 
</p>
<br />

<p>
<img width="750" alt="CVM RG6" src="https://github.com/user-attachments/assets/541f3928-a25c-473c-9b4e-e0ca9805304b" />
</p>
<p>
- After clicking Create you will be directed back to the RG section. You have successfully created your Resource Group in the Cloud. Now let's get to the good part and the real reason we're all here. To create some VMs! </p>
<br />

<h3> Step 2: Create a Windows VM in Azure </h3><p>
<img width="750" alt="CVM 1" src="https://github.com/user-attachments/assets/7666a0a4-96db-4742-980e-c2e4b255cb7d" />
</p>
<p>
- From this screen, locate the search bar again and enter "virtual". Select "Virtual machines" from the options populated. This will direct you to the Virtual Machines section.
</p>
<br />

<p>
<img width="750" alt="CVM 2" src="https://github.com/user-attachments/assets/608f7437-62b3-44ff-8bf0-0f0cb2da6c79" />
</p>
- Simply click the + Create button to get started. (Simular to when we created the Resource Group)
</p>
<br />

<p>
<img width="750" alt="CVM 3" src="https://github.com/user-attachments/assets/754c7d0d-b1d4-44e4-8514-9cb69fdba6c6" />
</p>
<p>
 - Select the first option, "Azure virtual machine" from the drop down and click + Create button.
</p>
<br />

<p>
<img width="750" alt="CVM 5" src="https://github.com/user-attachments/assets/eec90446-dfc6-4585-a148-f42cb3ee7b3d" />
</p>
<p>
 - Your subscription should already be selected.
 
 1. Choose the RG we created earlier.
 
 2. Name the VM "windows-vm".
    
 3. Select the same Region as before. "(US) East US 2". *We want the RG and Region to be the same for everything we are creating.*
    
 4. Select "Windows 10 Pro, version 22H2" for the Image. This will be the Operating System (OS) for the VM. *Do Not select a Windows Server*
</p>
<br />

<p>
<img width="750" alt"CVM 6" src="https://github.com/user-attachments/assets/8d66c106-64c0-4ad1-a9ec-0f0c5570a014" />
</p>
<p>
 - Scroll down to select the Size. We want to use the "Standard_D2s_v5 - 2 vcpus, 8 GiB memory".</p>
<p>- If you do not see this listed, click "See all sizes" to get more options. Sometimes the Region selected can cause this specific size to not populate. That is okay. Just make sure the size you pick has at least 2 vcpus and 8 GiB memory. This will be plenty of power to handle what we are doing. 😉
</p>
<br />

<p>
<img width="750" alt="CVM 7" src="https://github.com/user-attachments/assets/f881cb39-aef3-4eeb-affb-4466f22ad25a" />
</p>
<p>
 - Next, you will create a username and password for the VM. We will need this to log on later with a Remote Desktop Connection (RDP). *Highly recommend saving this infomation to refer back to later.*</p>
<p>- Now, locate the Licensing area towards the bottom of the screen. You will need to check the box to confirm. This is required because we are creating a Windows VM. Deployment will not work if left unchecked. Click "Next: Disks" to move on.
</p>
<br />

<p>
<img width="750" alt="CVM 8" src="https://github.com/user-attachments/assets/462d11fb-f8f0-4219-9c26-827170912aea" />
</p>
<p>
 - We will leave the Disks settings at Default for what we are doing, but you can see all the differnet options Azure provides. Click "Next: Networking" to move on to Networking. This is where we will set the Vitrual Network for the VM.
</p>
<br />

<p>
<img width="750" alt="CVM 9" src="https://github.com/user-attachments/assets/53c79197-e802-42a6-a97a-0108ec3357bb" />
</p>
<p>
 - Azure may auto populate a Network name for you. Go ahead and create a new one with a name of your choosing. Just note what you named the Network to refer back to later. We will need it for the Linux VM. You can leave the rest at Default setting. Azure will automatically assign the Subnet and Public IP for you. Leave the RDP Port as well. We will need access the VM via Remote Desktop Connection later. Click "Review + create" button.
</p>
<br />

<p>
<img width="750" alt="CVM 10" src="https://github.com/user-attachments/assets/55bae108-9d45-494c-968f-0f6c39a8953c" />
</p>
<p>
 - Review all the informatiom for the Windows VM. Our Subsciption, RG, and Region are correct. We named the VM "windows-vm". The Image and Size are correct and we have RDP active. Simply click "Create".
</p>
<br />

<p>
<img width="750" alt="CVM 11" src="https://github.com/user-attachments/assets/faaeb121-7fcf-4e08-94a0-587eed4fd249" />
</p>
<p>
 - Once you click "Create", the Deployment of the Windows VM will begin. Grab a snack or something to drink beacuse this can take a few minutes. When you come back from snacking, you will see "Your deployment is complete". Congrats! We just created our first Virtual Machine in the Cloud but let's not get too excited. There is still work to be done. Click "Create another VM" to get started on the Linux VM.
</p>
<br />

<h3> Step 3: Create a Linux VM in Azure </h3>

<p>
<img width="750" alt="CVM 12" src="https://github.com/user-attachments/assets/5c86e766-a2cb-4000-80f9-11b397d97707" />
</p>
<p>
- Hey, this screen looks familiar... Select the same RG that we created earlier. Name the VM "linux-vm" and choose the same Region as before. Again, this will save you headaches in the future.
</p>
<br />

<p>
<img width="750" alt="CVM 13" src="https://github.com/user-attachments/assets/508c5b6f-1b67-405c-802b-206b422052cd" />
</p>
<p>
- Since this will be the Linux VM, select "Ubuntu Server 22.02" for the Image.
</p>
<br />

<p>
<img width="750" alt="CVM 14" src="https://github.com/user-attachments/assets/ddad7697-f8cf-4003-a93b-f1b040f82c65" />
</p>
<p>- Choose the same Size option as before. "Standard_D2s_v5 - 2 vcpus, 8 GiB memory". </p>
<p>- Next, you will need to select "Password" for Authentication type. Azure defaults to SSH public key. Then, create a Username and Password. You can use information as the Windows VM to keep it simple.Once you are done, scroll done and click "Disks". Leave these options as default and skip to "Networking". 
</p>
<br />

<p>
<img width="750" alt="CVM 15" src="https://github.com/user-attachments/assets/4c159176-e6da-444f-967a-dd0f6a6a5d40" />
</p>
<p>
- Make sure to select the same Virtual Network that we created earlier. We can leave everything else as default. Scroll down and click "Review + create".  
</p>
<br />

<p>
<img width="750" alt="CVM 16" src="https://github.com/user-attachments/assets/e81a268d-75e1-4031-b042-2c13e1e00586" />
</p>
<p>
- On the next screen you will see the deployment of the Linux VM in progress. Time for second snack. This may take a few minutes.  
</p>
<br />

<p>
<img width="750" alt="CVM 17" src="https://github.com/user-attachments/assets/c84c0ca9-20ca-408d-9662-5ccadc25c947" />
</p>
<p>
- The Linux VM has been successfully created. Let's Go! Locate the search bar at the top of the screen and type in "virtual". Select "Virtual machines" and you will be direct to your newly created VMs!  
</p>
<br />

<p>
<img width="750" alt="CVM 18" src="https://github.com/user-attachments/assets/a013313b-16e7-4d7e-80d1-35cabfce1582" />
</p>
<p>
- You can view the Windows and Linux VMs we created in the Cloud. You will notice the RG and Locations match, what OS they are running, Public IP addresses, and so much more... </p>
<p> *Pro Tip: Notice the Start, Restart, and Stop buttons above the OS and Size area. You can use these to "turn off", "turn on" , or "restart" the VMs like you would your physical PC or Laptop. To save on your subsricption, you can "Stop" the VMs from running while you are not using them. Just make sure to "Start" them when you are ready to use them again. If you want extra practice, you can simply delete the RG and recreate everything as needed.*   
</p>
<br />

<h2>✅ Conclusion</h2>

<p>
This concludes our project. We sucessfully created a Resource Group, a Windows VM running Windows 10 Pro, and a Linux VM running Unbutu in the Cloud. We got to learn and witness the many possibilties of what Cloud Computing and Virtualization offers. Now, we essentilly have three machines in total to use how we want for our IT needs. </p>
<p>I completed this from a Macbook and have gained access to 2 other machines running a differnet OS without taking up any desk space or shelling out thousands of dollars. You can clearly see the many benefits that companies gain from using Cloud Services and Cloud Service Providers (CSP). Don't forget to Stop (turn off) the VMs in Azure. Thank You for your time and viewing this Project. We'll see you on the next one! 😎      
</p>
<br />
