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

VirtualBox allows you create and run multiple virtual machines (VMs) simultaneously on a single physical computer. Below will be the link so you may download and install the software yourself 

<a href="https://www.virtualbox.org/wiki/Downloads">![virtual box](https://github.com/user-attachments/assets/b3395578-653e-4109-b868-6272013de321))<a/>


Describing the permissions string
The permissions string decides who is allowed to read ,write and execute files in the projects directory. The characters r=read, w=write, and x=execute are used as the permissions as above.

For the first character either directory (d) or a hyphen (-) is used. If a hyphen is the first character will mean that it's a regular file and if d would be directory.

After that, characters 2, 3, and 4 are the user permissions.  Which will contain characters r, w, x or a hyphen depending on the permissions. A hyphen (-) in characters 2-10 means the permission is not granted.

Then, characters 5, 6, and 7 are the group permissions. Which will contain characters r, w, x or a hyphen depending on the permissions. A hyphen (-) in characters 2-10 means the permission is not granted.

Lastly, characters 8, 9 ,10 represent permissions for other. For any other users on the system aside from user and group. Which will contain characters r, w, x or a hyphen depending on the permissions. A hyphen (-) in characters 2-10 means the permission is not granted.

Step 2:
Change file permissions.

Below, I changed permissions in the “other” group of characters in file “project_k.txt” and took away the write (w) permissions as that can pose a security risk. I did this by inputting the chmod command with the first argument (o-w) which will take away permissions from the second argument which is the file you want permissions changed.

![permissions2](https://github.com/VegaL101/File-permissions-lab./assets/166334918/64441a6d-b114-499f-a53d-e3c7a2745114)

Step 3:
Change file permissions on a hidden file.

Here, I change the permissions of a hidden file that has been archived named .project_x.txt. I am able to determine if a file is hidden or not because a hidden file begins with a period (.). Once again I entered the chmod command here to change multiple permissions at once. But this time I also added group reading permissions (g+r) permissions instead of just taking away permission (u-w,g-w). I still left reading permissions in case the file still needs to be viewed for any reason.

![permissions3](https://github.com/VegaL101/File-permissions-lab./assets/166334918/1f4a4e9c-20e5-43f6-80c9-53c4e8e32158)

Step 4:
Change directory permissions.

Next, I had to change the drafts directory permissions so only researcher2 had access to it. I realized that the group had the execute permissions. So I input the chmod command to take them away (g-x) as seen above.

![permissions4](https://github.com/VegaL101/File-permissions-lab./assets/166334918/b297a9a2-3b2b-4bb4-a678-d0f1b0d6af38)

## Summary
Multiple permissions have been changed to reflect the level of authority the organization intended for. Firstly, I checked file permissions with  ls -la which showed a list of permissions before any changes were made which was needed so that updates to permissions can be made.  Write permissions for other on file project_k.txt have been taken away.  Write permissions for user and group have been removed and read permissions for group have been added for hidden file .project_x.txt. Execute permissions for group have been taken away from directory drafts so that only researcher2 has access to it.



