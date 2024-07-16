# Setting-up-a-basic-home-lab

## Objective
The objective of this project is to set up a basic home lab so that you may test tools, simulate attacks, and analyze malware safely.


### Skills Learned

- Learned how to install virtual machines such as Ubuntu and Kali Linux .
- Learned how to take snapshots and create clones of your virtual machines.
- Learned how to update and update Virtual Machines.
- Learned How to appropriatley configure network settings on virtualBox depending on your needs.

## Steps

Step 1:
Downlaod and install VirtualBox.

VirtualBox allows you create and run multiple virtual machines (VMs) simultaneously on a single physical computer. Clicking the image below will direct you to their website so you may download and install the software yourself 

<a href="https://www.virtualbox.org/wiki/Downloads"><img src="https://github.com/user-attachments/assets/ed49af36-1b5c-44d3-b9df-4ebfe148e32a"></a>

Step 2:
Download The Ubuntu and Kali-Linux ISO image.

A ISO image is typically used for installing a operating system in a computer. We will be using the Ubuntu and the Kali-Linux ISO image to create virtual machines with these operating systems. The images below will direct you to their respective websites, where you can download them.

Ubuntu:

<a href="https://ubuntu.com/download/desktop#how-to-install"><img src="https://github.com/user-attachments/assets/93922b10-cbbf-4581-91f5-4f6f359706dc" width="600" height="350"></a>

Kali-Linux:

<a href="https://www.kali.org/get-kali/#kali-installer-images"><img src="https://github.com/user-attachments/assets/8e975e6b-6306-4b07-abd9-7d58f5612214" width="600" height="350"></a>

for Kali-Linux you will need to choose the installer Version.

Step 3:
Create your virtual machihnes.

Here, we will begin creating your virtual machines. first, when you open virtual box you should be presented with the screen below.
you will then click on "machine" on the top left corner and then click "new" to get started.

![virtualbox menu](https://github.com/user-attachments/assets/cbe41dc7-3f33-4570-b570-b63cc8b8829d)
##
Then, the screen below will pop up. Here, you can name your virtual machine and select the ISO image you want to use for that VM. Make sure you click "skip unattended installation". Once you are done with that you can proceed and click "next".

![vm creator](https://github.com/user-attachments/assets/3e8aa435-d0b0-400a-9a3e-37543320e72e)
##
Next you can choose the hardware for your VM such as memory and processors. 1 CPU is normally more than enough for a basic home lab. When creating a virtual machine, it's important to consider that it will utilize resources from your host machine to operate efficiently. Therefore, be considerate of your host machine. 

![vm creator 2](https://github.com/user-attachments/assets/dc7b732e-261d-4467-a3cc-de3a881088f4)
##
Once you've made your hardware selections, you can now configure your virtual hardisk (storage thats tied to your VM). You have the option to configure the size of the virtual hard disk, utilize an existing virtual hard disk file (which can be shared with another VM), or choose not to add a virtual hard disk.

![vm creator 3](https://github.com/user-attachments/assets/9f9d58f3-a522-4190-8112-bfa7c0198ced)
##
After completing the steps above, you'll reach a summary of the VM settings where you can review your choices before finalizing them. Clicking "Finish" will boot-up of your VM. Depending on the ISO image you selected, you will proceed to set up your new operating system and create a user on the VM.

![vm creator 4](https://github.com/user-attachments/assets/565885f9-27c7-4645-835d-0d12f7ddefe8)

Step 4:
Update and upgrade your VM.

Once you've opened your VM and are ready to start, one of the first essential tasks is to update your system. To do this, open a terminal and enter the following command: 'sudo apt update && sudo apt upgrade -y'.
This will ensure that your system's package lists are updated (sudo apt update). In the next segment the command proceeds to upgrade all installed packages to their latest versions (sudo apt upgrade -y). You can input this command in both Kali - Linux and Ubuntu.

![ubuntu update](https://github.com/user-attachments/assets/addd36ff-4cab-41b6-a78b-c987533dd2e6)

Step 5:
Configure your network settings


In this step, we will configure the network settings to suit your needs. As an example, we will set up a NAT network.

 first, click on "File," then navigate to "Tools" and select "Network Manager." Choose "NAT Network" from the options presented. Your screen should resemble the image depicted below. Next, right-click to create a new NAT Network configuration. This setup allows you to tailor network settings to your specific needs, ensuring your virtual environment is configured appropriately.

![networks menu](https://github.com/user-attachments/assets/a8c22ba9-8eb6-46c9-bc4a-613791f7bb04)


Next we will configure network settings for your desired virtual machine (VM), follow these steps:
Click on the VM you want to configure, then navigate to "Settings" and select "Network."
In the Network settings,choose the dropdown menu labeled "Attached to". Click on it and select "NAT Network" to change your VM's network configuration to NAT Network.
Next, click on the dropdown menu labeled "Name" and choose The NAT Network you created earlier .
By default, VMs are set to use NAT, which is good for basic tasks like testing tools. Both NAT and NAT Network configurations provide internet access through the host machine's network connection.
However, NAT Network additionally allows VMs to communicate with each other, which can be useful in certain scenarios.

![kali nat network](https://github.com/user-attachments/assets/a5e6ad43-ec99-4aac-b4de-023b51d2b4ff)

One thing to note is that using these network settings for analyzing malware is not recommended, as it can potentially harm your host machine. For safe analysis, it is recommended to use an "Internal Network" or set the VM to "Not Attached" (no network) to isolate it completely.

## Summary
Multiple permissions have been changed to reflect the level of authority the organization intended for. Firstly, I checked file permissions with  ls -la which showed a list of permissions before any changes were made which was needed so that updates to permissions can be made.  Write permissions for other on file project_k.txt have been taken away.  Write permissions for user and group have been removed and read permissions for group have been added for hidden file .project_x.txt. Execute permissions for group have been taken away from directory drafts so that only researcher2 has access to it.



