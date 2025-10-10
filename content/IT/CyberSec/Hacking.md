[Wireshark](https://drive.google.com/drive/u/0/folders/1pu1fhfZhv0GNO227Br-NofQ2r7ob0gZA)
[It Security and Ethical hacking](https://drive.google.com/drive/u/0/folders/1YvsUgarl8PZwcUmxdrIBwEXDATzT2NFE)
[Udemy Certified white hat hacker](https://drive.google.com/drive/u/0/folders/1TEiC6Nr6jx9WuLR2zeMh0qjV5AVtMc9s)
[Hacking 2018](https://drive.google.com/drive/u/0/folders/1enAyu5mN4ykS-67oC5vkDBbiyeQHuS_t)
https://explainshell.com/


[[Hacking.excalidraw]]


#todo Familiarizing ourselves with each of these security frameworks

|   |   |
|---|---|
|Credit Card Account Information|`Payment Card Industry` (`PCI`)|
|Electronic Patient Health Information|`Health Insurance Portability and Accountability Act` (`HIPAA`)|
|Consumers Private Banking Information|`Gramm-Leach-Bliley` (`GLBA`)|
|Government Information|`Federal Information Security Management Act of 2002` (`FISMA`)|

|                                                                     |                                                                            |
| ------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| (`NIST`) - National Institute of Standards and Technology           | (`CIS Controls`) - Center for Internet Security Controls                   |
| (`ISO`) - International Organization for Standardization            | (`PCI-DSS`) - The Payment Card Industry Data Security Standard             |
| (`GDPR`) - General Data Protection Regulation                       | (`COBIT`) - Control Objectives for Information and Related Technologies    |
| (`FedRAMP`) - The Federal Risk and Authorization Management Program | (`ITAR`) - International Traffic in Arms Regulations                       |
| (`AICPA`) - American Institute of Certified Public Accountants      | (`NERC CIP Standards`) - NERC Critical Infrastructure Protection Standards |


## Privilege Escalation Linux

### Folders
- opt - optional programs
- bin - shared programs
- sbin - system programs
- tmp - all users writable folder
- etc - config files
- var - logs


`ls -lah` - last modified and permissions

### Changing permissions
`u` - users
`g` - groups
`o` - others
`a` - all

`+` add perms
`-` remove perms
```bash
# overwrite
sudo chmod u=rwx file.txt
```


```bash
cat /etc/passwd

root:x:0:0:root:/root:/bin/ash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
```
![[passwd.png]]

user ids: 
- 1-99 - Other predefined accounts
- 100-999 - Admin and system accounts
- 1000 - ... Regular users

```bash
cat /etc/shadow

raj:$y$j9T$5KGIS/2Ug.47GjW0jHOIB/$XwYUafYPh/petN8gKSJuLt5CEbBya3dW3pIgwrS3eJB:19447:0:99999:7:::
```

![TecAdmin](https://tecadmin.net/wp-content/uploads/2022/12/linux-etc-shadow-file.png)
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh0jcVfiqHr6gUk36CPjo_iDCSwgmPvniJ1fsJwrpw0Fryms8HeYUVJh6sJ3GNzxwVcfDO9_jBN2aJ7LKg2ZmsBhwhwJf0Cl-NBAWTPz6GLe7A55xZ6ZECTjJuQ4Q4ZGPPOcsu5ewiGlyI/s1600/tux_etc_passwd.jpg)

```bash
cat /etc/group

```

![](https://devconnected.com/wp-content/uploads/2019/09/etc-group-file.png)