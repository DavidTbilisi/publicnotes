#it/hacking #windows

How many versions of Windows are there? ==9 versions==
??

| Operating System Names               | Version Number |
| ------------------------------------ | -------------- |
| Windows NT 4                         | 4.0            |
| Windows 2000                         | 5.0            |
| Windows XP                           | 5.1            |
| Windows Server 2003, 2003 R2         | 5.2            |
| Windows Vista, Server 2008           | 6.0            |
| Windows 7, Server 2008 R2            | 6.1            |
| Windows 8, Server 2012               | 6.2            |
| Windows 8.1, Server 2012 R2          | 6.3            |
| Windows 10, Server 2016, Server 2019 | 10.0           |


Gets [instances](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1) of Windows Management Instrumentation
```powershell-session
Get-WmiObject -Class win32_OperatingSystem
```

| Directory                  | Function                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Perflogs                   | Can hold Windows performance logs but is empty by default.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Program Files              | On 32-bit systems, all 16-bit and 32-bit programs are installed here. On 64-bit systems, only 64-bit programs are installed here.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Program Files (x86)        | 32-bit and 16-bit programs are installed here on 64-bit editions of Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ProgramData                | This is a hidden folder that contains data that is essential for certain installed programs to run. This data is accessible by the program no matter what user is running it.                                                                                                                                                                                                                                                                                                                                                                                                  |
| Users                      | This folder contains user profiles for each user that logs onto the system and contains the two folders Public and Default.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Default                    | This is the default user profile ==template== for all created users. Whenever a new user is added to the system, their profile is based on the Default profile.                                                                                                                                                                                                                                                                                                                                                                                                                |
| Public                     | This folder is intended for computer users to ==share files== and is accessible ==to all users by default==. This folder is shared over the network by default but requires a valid network account to access.                                                                                                                                                                                                                                                                                                                                                                 |
| AppData                    | Per user application data and settings are stored in a hidden user subfolder (i.e., cliff.moore\AppData). Each of these folders contains three subfolders. The ==Roaming== folder contains ==machine-independent data== that should follow the user's profile, such as custom dictionaries. The ==Local folder== is specific to the computer itself and is ==never synchronized across the network==. LocalLow is similar to the Local folder, but it has a lower data integrity level. Therefore it can be used, for example, by a web browser set to protected or safe mode. |
| Windows                    | The majority of the files required for the Windows operating system are contained here.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| System, System32, SysWOW64 | Contains all DLLs required for the core features of Windows and the Windows API. The operating system searches these folders any time a program asks to load a DLL without specifying an absolute path.                                                                                                                                                                                                                                                                                                                                                                        |
| WinSxS                     | The Windows Component Store contains a copy of all Windows components, updates, and service packs.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

## File System
What does FAT means?  ==File Allocation Table==
<!--SR:!2025-01-08,3,250-->

How many File System supports windows?
?
FAT12
FAT16
FAT32
NTFS
exFAT.
<!--SR:!2025-01-06,1,230-->


## Access Control Lists (ACLs) aka Permissions 

Full Control - 
Modify - 
List Folder Contents - 
Read and Execute - 
Write - 
Read - 
Traverse Folder - 

## Integrity Control Access Control List (icacls)


3 page
home default
products - show products list
products/id - details

[[regedit]]



## UG Exam
#uni_of_georgia
[[Windows.excalidraw]]