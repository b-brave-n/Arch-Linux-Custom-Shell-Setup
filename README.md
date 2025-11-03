# Arch Linux Custom Shell Setup
Step-by-step guide to installing and configuring the Fish shell on a fresh Arch Linux installation for MacOS users.

**Table of Contents** <br>
	•	Prerequisites <br>
  •	Arch Linux Setup <br>
	•	Arch Linux Installation <br>
	•	Common Post-Install Customization <br>
	•	Reverting to a Different Shell <br>
	•	References<br>



<br><br>
**Prerequisites**

1. Download VirtualBox app file using the link: https://www.virtualbox.org/wiki/Downloads.<br>
2. Download an unofficial ARM-based ISO file from: https://release.archboot.com/aarch64/latest/iso/
3. Install VirtualBox app.



<br><br>
**Arch Linux Setup** <br>

1. Open VirtualBox
2. Click "New"
3. Select VM Name
4. Select ISO Image file and select the file you have downloaded
5. Select ARM 64-bit

Click "Next" to Continue <br> 
<img width="967" height="491" alt="Screenshot 2025-11-02 at 11 42 38 PM" src="https://github.com/user-attachments/assets/297b2cae-3223-4427-9042-2fa0dfa8a8f7" /><br><br>

1. Allocate "Base Memory"(e.g. 8192MB)
2. Allocate "Number of CPUs" (10)
3. Allocate "Disk Size" (e.g. 20.00GiB) <br>
<img width="964" height="488" alt="Screenshot 2025-11-02 at 11 43 57 PM" src="https://github.com/user-attachments/assets/afa66951-7c27-4946-8b84-d350dd5dee66" /><br><br>

Click "Next" to Continue <br>
<img width="965" height="489" alt="Screenshot 2025-11-02 at 11 49 26 PM" src="https://github.com/user-attachments/assets/083b68fe-4ebe-4f6e-8479-70dab98a36c5" /><br><br>

Click "Finish"


<br><br>
**Arch Linux Installation** <br>

1. Start the VM
2. Select Language
3. Click on "Launch UEFI Archboot"
4. Hit Enter to start
5. Select Locale Language
6. Select "No" to Online Mode <br>
         <img width="313" height="69" alt="image" src="https://github.com/user-attachments/assets/90468b86-3a85-4281-9073-238576db0416" />
<br><br>
7. Select Timezone & Region
8. Select "Launch Archboot Setup"
   <br>
          <img width="278" height="122" alt="image" src="https://github.com/user-attachments/assets/c01621ac-a37c-4509-8997-1f8fed91413e" /><br><br><br><br><br><br>
9. Select "Preparing Storage Device"
<br>
		<img width="1070" height="520" alt="image" src="https://github.com/user-attachments/assets/275ab717-1b08-41f5-a903-f8b3db00e6a4" />
<br><br>
11. Select "Quick Setup"
12. Select "/dev/sda {your allocated memory}"
13. Select "PARTUUID=<partuuid>"
14. Select "/efi MULTIBOOT"
15. Enter Disk space you want to allocate for "EFI System Partition (ESP)".
    <br>
          <img width="452" height="110" alt="image" src="https://github.com/user-attachments/assets/4efa2480-0091-4505-be46-36ad75e4903c" /><br><br>
16. Enter Disk space you want to allocate for "EXtended Bootloader Partition (XBOOTLDR)".
    <br>
          <img width="452" height="107" alt="image" src="https://github.com/user-attachments/assets/b731ceca-4f15-4a26-bd6c-105ef1710f6a" /><br><br>
17. Enter Disk space you want to allocate for "SWAP".
    <br>
          <img width="454" height="105" alt="Screenshot 2025-11-03 at 12 16 07 AM" src="https://github.com/user-attachments/assets/2a8abbf0-9e69-4607-896d-3acac470b313" /><br><br>
18. Select "ext4 Ext4" in Filesystem and home
    <br>
          <img width="315" height="138" alt="image" src="https://github.com/user-attachments/assets/21848b03-4f2f-4694-a7c8-e9beda4e841b" /><br><br>
19. Confirm the file system you want to use.
20. Allocate your disk space for _/home_ directory
21. Confirm it!
22. Authorize the deletion of ALL DATA in on _/dev/sda_
    <br><br>
          <img width="315" height="138" alt="image" src="https://github.com/user-attachments/assets/59efa294-2ae6-4fe5-9147-34c24557af97" />
<br><br><br>

23. Select "Install Packages"
    <br>
<img width="537" height="260" alt="Screenshot 2025-11-03 at 12 40 32 AM" src="https://github.com/user-attachments/assets/30623b3c-50e1-4399-a72d-f6c7626dd683" />

<br><br><br>
24. Select "Yes"<br><br>
25. Select "Configur System"
<br><img width="537" height="260" alt="Screenshot 2025-11-03 at 12 44 58 AM" src="https://github.com/user-attachments/assets/90cc17d7-197c-47c2-9cd6-f19c995d6bc8" />
<br><br><br>
26. Select a "New Root Password" and confirm it><br>
27. Select "NANO" for Text editor so it will be easier for us to learn><br>
28. Select "BUSYBOX"><br>
29. Set Default Shell to "Standard Base Shell"><br>
30. Select "Create a User Account" and create username and "Enable user as Admin and Part of wheel group."><br>
<br><img width="207" height="111" alt="image" src="https://github.com/user-attachments/assets/96ae401b-d205-4c44-97c8-49f0ad46398b" /><br><br>
31. Select password for your user><br>
32. "Return to System Configuration"><br>
<img width="280" height="139" alt="Screenshot 2025-11-03 at 12 54 38 AM" src="https://github.com/user-attachments/assets/bd97b92b-b3c9-4ee5-993a-6eb0463f9c10" /><br><br>
33. Select _"/etc/locale.conf"_ <br>
34. If file is empty, type _"LANG=en_US. UTF-8"_. Save and exit <br>
35. Select _"/etc/locale.gen"_ and uncomment the en_US.UTF-8 UTF-8 (Shortcut for searching: Ctrl+W) <br>
36. Select _"/etc/hostname"_ and change it to the name of your choice (eg. github) <br>
<img width="113" height="60" alt="Screenshot 2025-11-03 at 1 05 12 AM" src="https://github.com/user-attachments/assets/ea6ac892-4cdb-4bd1-8f01-3278d1c4d4f3" /> <br><br>
37. Select _"/etc/hosts"_ and add the line _127.0.1.1	{github}.localdomain	{github}_ <br> without deleting anything
<br> <img width="333" height="91" alt="Screenshot 2025-11-03 at 1 08 52 AM" src="https://github.com/user-attachments/assets/7c5f4a0c-813e-4db7-97e9-61fe4e8a69d3" /> <br><br>
38. Select "Back" <br>
39. Select "Install Bootlader" <br>
<img width="315" height="152" alt="Screenshot 2025-11-03 at 1 11 01 AM" src="https://github.com/user-attachments/assets/2dc8bb4c-9bf0-4702-a00d-e7f58119e6ed" /> <br><br>
40. Select "GRUB UEFI" <br>
41. Select "OK" to continue <br>
42. Without changing any line, exit the file (Ctrl+X) <br>
43. Select "Reboot System" and log in to your account again <br>
<img width="208" height="121" alt="Screenshot 2025-11-03 at 1 17 25 AM" src="https://github.com/user-attachments/assets/9178ad6d-f149-4fa8-a6cf-8b6cee787e41" /> <br> <br>
44. 
