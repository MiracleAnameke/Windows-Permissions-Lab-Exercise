# Windows Permissions Lab Exercise

## Description
This lab exercise guides students through the exploration of permissions for Windows securable objects, using practical examples on different versions of Windows operating systems. By the end of this lab, students will have a deeper understanding of NTFS permissions, Access Control Lists (ACLs), and how permissions affect file access and system security.

## Requirements
- Windows Server 2008 R2 VM
- Windows 7 VM
- Windows 10 VM
- Domain Administrator access

## Lab Steps and Screenshots

### Slide 1: VM Network Configuration and Connectivity Test
Perform `net config workstation` and ping the other VMs from the Windows Server 2008 R2 VM.
<p align="center">
  <img src="https://i.imgur.com/lxAdA72.png" height="80%" width="80%" alt="Slide 1 Screenshot"/>
</p>

### Slide 2: VM Network Configuration and Connectivity Test
Perform `net config workstation` and ping the other VMs from the Windows 7 VM.
<p align="center">
  <img src="https://i.imgur.com/7imSX3q.png" height="80%" width="80%" alt="Slide 2 Screenshot"/>
</p>

### Slide 3: VM Network Configuration and Connectivity Test
Perform `net config workstation` and ping the other VMs from the Windows 10 VM.
<p align="center">
  <img src="https://i.imgur.com/KdnKDQl.png" height="80%" width="80%" alt="Slide 3 Screenshot"/>
</p>

### Slide 4: NTFS Permissions on Windows 7 VM
Show the INFO6003 folder, Sub1 folder, and File1 file after setting NTFS permissions.
<p align="center">
  <img src="https://i.imgur.com/Z2qXLVJ.png" height="80%" width="80%" alt="Slide 4 Screenshot"/>
</p>

### Slide 5: Advanced NTFS Permissions
Demonstrate advanced permission settings, including denying and allowing permissions for different users.
<p align="center">
  <img src="https://i.imgur.com/AaLSAW2.png" height="80%" width="80%" alt="Slide 5 Screenshot"/>
</p>

### Slide 6: Command Line ACL Management
Using the command line, manage the ACL for the INFO6003 directory and contents.
<p align="center">
  <img src="https://i.imgur.com/CKEcmgz.png" height="80%" width="80%" alt="Slide 6 Screenshot"/>
</p>

### Slide 7: File Sharing and NTFS Permissions
Show the shared folder on the server and the NTFS permissions assigned to each user.
<p align="center">
  <img src="https://i.imgur.com/dwHHe8b.png" height="80%" width="80%" alt="Slide 7 Screenshot"/>
</p>

## Conclusion
This lab provides practical skills in managing file and system permissions across a Windows network environment.

## Additional Information

### File Share Security Options Include:

- **Read**: Allows viewing file/folder contents and executing files.
- **Change**: Includes "Read" permissions and additionally allows adding, modifying, and deleting files and subfolders.
- **Full Control**: Grants all permissions, including changing permissions and taking ownership.
- **Deny**: Explicitly denies the selected permissions, overriding any "Allow" permissions.

### Why Do We Use File Share on the Network?

- **Centralized Storage**: Allows files and folders to be stored in a central location, making it easier to manage, backup, and maintain.
- **Collaboration**: Enables multiple users to access, collaborate, and work on files simultaneously.
- **Access Control**: Provides the ability to control who can access files and what they can do with them using permissions.
- **Resource Optimization**: Reduces the need for multiple copies of files on individual computers, saving storage space.
- **Backup and Recovery**: Centralized storage makes it easier to implement backup and disaster recovery solutions.

### If Both File Share and NTFS Security Are on a Folder, Which Security Is Applied to the User Who Has Access?

When both share permissions and NTFS permissions are configured, the most restrictive of the two applies. For example, if share permissions allow "Full Control" but NTFS permissions only allow "Read", the user will only have "Read" access when accessing the folder over the network. If accessing the folder directly on the server (locally), only the NTFS permissions apply.

---

