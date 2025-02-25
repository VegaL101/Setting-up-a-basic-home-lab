# Setting-up-a-basic-home-lab

## Objective
The objective of this project is to set up a basic home lab so that you may test tools, simulate attacks, and analyze malware safely.


### Skills Learned

- Learned how to install virtual machines such as Ubuntu and Kali Linux .
- Learned how to take snapshots so it may serve as a baseline.
- Learned how to update and update Virtual Machines.
- Learned How to appropriatley configure network settings on virtualBox depending on your needs.

## Steps

Step 1:
Downlaod and install VirtualBox.

VirtualBox allows you create and run multiple virtual machines (VMs) simultaneously on a single physical computer. Clicking the image below will direct you to their website so you may download and install the software yourself 

<a href="https://www.virtualbox.org/wiki/Downloads"><img src="https://github.com/user-attachments/assets/ed49af36-1b5c-44d3-b9df-4ebfe148e32a"></a>
##
Step 2:
Download The Ubuntu and Kali-Linux ISO image.

An ISO image is commonly used to install an operating system on a computer. In this case, we'll be using Ubuntu and Kali Linux ISO images to set up virtual machines with these operating systems. By clicking on the images below, you'll be directed to their respective websites where you can download the images.

Ubuntu:

<a href="https://ubuntu.com/download/desktop#how-to-install"><img src="https://github.com/user-attachments/assets/93922b10-cbbf-4581-91f5-4f6f359706dc" width="600" height="350"></a>

Kali-Linux:

<a href="https://www.kali.org/get-kali/#kali-installer-images"><img src="https://github.com/user-attachments/assets/8e975e6b-6306-4b07-abd9-7d58f5612214" width="600" height="350"></a>

for Kali-Linux you will need to choose the installer Version.
##
Step 3:
Create your virtual machines.

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
##
Step 4:
Update and upgrade your VM.

Once you've opened your VM and are ready to start, one of the first essential tasks is to update your system. To do this, open a terminal and enter the following command: 'sudo apt update && sudo apt upgrade -y'.
This will ensure that your system's package lists are updated (sudo apt update). In the next segment the command proceeds to upgrade all installed packages to their latest versions (sudo apt upgrade -y). You can input this command in both Kali - Linux and Ubuntu. 
![ubuntu update](https://github.com/user-attachments/assets/addd36ff-4cab-41b6-a78b-c987533dd2e6)

You will also need this final command only for Ubuntu. This will install any essential updates for Ubuntu.

![ubuntu tools](https://github.com/user-attachments/assets/4d7ffa67-7418-4b97-8ce9-69c9ca33e02e)
##
Once you have updated your VM, it's imprtant to create your first snapshot to establish a baseline. Baselines are pivotal for monitoring performance, troubleshooting issues, managing changes effectively, and serving various other purposes. They ensure stability and efficiency for your VM.
To take a snapshot you are gonna have to Select your desired VM and locate the "Take" button at the top, resembling a camera icon.
Click on this button.

![baseline](https://github.com/user-attachments/assets/9ccdb6f8-0942-41be-b834-e20c07a6ffed)

 Give your snapshot a name, typically something like "baseline 1," and a brief description if needed.Click "Ok" to confirm and complete the snapshot creation process.
By taking this snapshot, you capture the current state of your VM post-update. This snapshot serves as a baseline reference, enabling you to revert to this stable state if necessary.
##
Step 5:
Configure your network settings

In this step, we will configure the network settings to suit your needs. As an example, we will set up a NAT network.
 first, click on "File," then navigate to "Tools" and select "Network Manager." Choose "NAT Network" from the options presented. Your screen should resemble the image depicted below. Next, right-click to create a new NAT Network configuration. This setup allows you to tailor network settings to your specific needs, ensuring your virtual environment is configured appropriately.

![networks menu](https://github.com/user-attachments/assets/a8c22ba9-8eb6-46c9-bc4a-613791f7bb04)


Next we will configure network settings for your desired virtual machine (VM), follow these steps:
Click on the VM you want to configure, then navigate to "Settings" and select "Network."
In the Network settings,choose the dropdown labeled "Attached to". Go down it and select "NAT Network" to change your VM's network to a NAT Network.
Now, on the dropdown menu labeled "Name" you choose The NAT Network you created earlier.

![kali nat network](https://github.com/user-attachments/assets/a5e6ad43-ec99-4aac-b4de-023b51d2b4ff)

By default, VMs are set to use NAT, which is good for basic tasks like testing tools. Both NAT and NAT Network configurations provide internet access through the host machine's network connection.
However, NAT Network additionally allows VMs to communicate with each other. <br>One thing to note is that using these network settings for analyzing malware is not recommended, as it can potentially harm your host machine. For safe analysis, it is recommended to use an "Internal Network" or set the VM to "Not Attached" (no network) to isolate it completely.

## Summary
Upon completing the steps above, you will have successfully created a home lab environment ready for testing and learning. Throughout this project, we effectively installed all necessary components to create and update our VM, established a baseline configuration, and configured network settings to suit specific needs. This setup provides a solid framework for experimentation and understanding the workings of various technologies within a controlled environment.



