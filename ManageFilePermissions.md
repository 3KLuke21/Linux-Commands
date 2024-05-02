# File permissions in Linux

### Project description
The scenario involves identifying files with incorrect permissions and modifying them accordingly. Specifically, we need to ensure that no one except the user has write access to certain files, such as `.project_x.txt`, which is a hidden file in the research team's archive. Additionally, only the user `researcher2` should have access to the `drafts` directory and its contents.

### Check file and directory details
Using the `ls -la` command, we examined all permissions and hidden files within the directory.


<img width="648" alt="List of all files and permissions" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/591a7254-3fe8-4825-b401-7ad71a336618">

### Permissions string
We analyzed the 10-character string representing permissions, with each character indicating read, write, or execute access for the user, group, and others.


<img width="648" alt="10 character" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/377a70f0-42c7-4418-a380-f1162e281219">

Each character has a meaning:
* `d`: If it is a directory
* `r`: Permission to read
* `w`: Permission to write
* `x`: Permission to execute \
*Note: When the user hasn't got the permission, a dash "`-`" will be displayed instead.* \
\
Also, there are 3 sets of `rwx`
* The first set represents the main **User**'s permission;
  * ***User** represented by the letter `u`*
* The second represents the permissions of a **Group** of users;
  * ***Group** represented by the letter`g`* 
* The third and final set, represents permission for all **Other** users;
  * ***Other** represented by the letter`o`*


<img width="648" alt="image" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/97127ad1-e409-48df-b003-edf0b800852d"> 

### Change file permissions
Utilizing the `chmod` command, we modified permissions by adding or removing access using the `+` or `-` sign, respectively.


<img width="648" alt="image" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/710aa394-ff22-494c-ada0-1270d1fb2542">\

*In the exemple above, I used `chmod o-w` to removed the **write** access from the user **other***.


### Change file permissions on a hidden file
To adjust permissions for hidden files, we followed the same procedure, adding a `.` before the file name to denote its hidden status.


<img width="648" alt="image" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/2ebb9b3e-5f2a-43e1-9175-651cb177acdc">


### Change directory permissions
Similar to files, we altered directory permissions using the `chmod` command.


<img width="648" alt="image" src="https://github.com/3KLuke21/LinuxCommands_ManageFilePermissions/assets/50923722/c1c9959d-7bef-479a-9209-acc2d1a525a7">


### Summary
In summary, we adhered to organizational rules by adjusting permissions as required, ensuring that only authorized users have access to specific files and directories.
