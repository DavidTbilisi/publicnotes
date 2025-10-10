**Regedit** (short for **Registry Editor**) is a built-in tool in Windows that allows you to view, edit, and manage the Windows **Registry**. The registry is a hierarchical database that stores ==low-level settings== for the Windows operating system and applications. 

It contains configuration data for:
- hardware, 
- software, 
- user preferences,  
- system settings.

### Key Features of Regedit:

1. **View and Edit Registry Keys and Values**:
    
    - You can explore and modify specific settings that affect how Windows and installed programs operate.
2. **Add or Delete Keys**:
    
    - You can create new keys or delete existing ones to configure system behavior.
3. **Backup and Restore**:
    
    - Before making changes, you can back up registry keys to avoid system issues.

---

### When and Why Use Regedit:

- **Troubleshooting**: Fix errors by modifying registry settings.
- **Customization**: Change default system behaviors or software settings.
- **Performance Tweaks**: Improve system performance by adjusting specific registry keys.
- **Enable/Disable Features**: Activate or deactivate hidden features in Windows.

---

### Warning:

Editing the registry can be risky. Incorrect changes may lead to system instability or even prevent Windows from starting. Always back up the registry before making changes. You can back up by selecting **File > Export** in Regedit.

To open Regedit:

1. Press `Win + R` to open the Run dialog.
2. Type `regedit` and press Enter.
3. You’ll be prompted for administrator permission; click **Yes**.


## Root Keys

| Name                | Abbr | Most used              |
| ------------------- | ---- | ---------------------- |
| HKEY_CURRENT_USER   | HKCU | Backward compatibility |
| HKEY_USERS          | HKU  | Current user           |
| HKEY_CLASSES_ROOT   | HKCR | Used                   |
| HKEY_LOCAL_MACHINE  | HKLM | Used                   |
| HKEY_CURRENT_CONFIG | KHCC | Backward compatibility |


![[Registry_VS_File_storage.png]]