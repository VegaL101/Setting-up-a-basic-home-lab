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

Then, the screen below will pop up. Here, you can name your virtual machine and select the ISO image you want to use for that VM. Make sure you click "skip unattended installation". Once you are done with that you can proceed and click "next".

![vm creator](https://github.com/user-attachments/assets/3e8aa435-d0b0-400a-9a3e-37543320e72e)

Next you can choose the hardware for your VM such as memory and processors. 1 CPU is normally more than enough for a basic home lab. When creating a virtual machine, it's important to consider that it will utilize resources from your host machine to operate efficiently. Therefore, be considerate of your host machine. 

![vm creator 2](https://github.com/user-attachments/assets/dc7b732e-261d-4467-a3cc-de3a881088f4)

Once you've made your hardware selections, you can now configure your virtual hardisk (storage thats tied to your VM). You have the option to configure the size of the virtual hard disk, utilize an existing virtual hard disk file (which can be shared with another VM), or choose not to add a virtual hard disk.

![vm creator 3](https://github.com/user-attachments/assets/9f9d58f3-a522-4190-8112-bfa7c0198ced)

After completing the steps above, you'll reach a summary of the VM settings where you can review your choices before finalizing them. Clicking "Finish" will boot-up of your VM. Depending on the ISO image you selected, you will proceed to set up your new operating system and create a user on the VM.

![vm creator 4](https://github.com/user-attachments/assets/565885f9-27c7-4645-835d-0d12f7ddefe8)







Step 4:
Change directory permissions.

Next, I had to change the drafts directory permissions so only researcher2 had access to it. I realized that the group had the execute permissions. So I input the chmod command to take them away (g-x) as seen above.

![permissions4](https://github.com/VegaL101/File-permissions-lab./assets/166334918/b297a9a2-3b2b-4bb4-a678-d0f1b0d6af38)

## Summary
Multiple permissions have been changed to reflect the level of authority the organization intended for. Firstly, I checked file permissions with  ls -la which showed a list of permissions before any changes were made which was needed so that updates to permissions can be made.  Write permissions for other on file project_k.txt have been taken away.  Write permissions for user and group have been removed and read permissions for group have been added for hidden file .project_x.txt. Execute permissions for group have been taken away from directory drafts so that only researcher2 has access to it.



