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
          <img width="278" height="122" alt="image" src="https://github.com/user-attachments/assets/c01621ac-a37c-4509-8997-1f8fed91413e" /><br><br>
9. Select "Preparing Storage Device"
10. Select "Quick Setup"
11. Select "/dev/sda {your allocated memory}"
12. Select "PARTUUID=<partuuid>"
13. Select "/efi MULTIBOOT"
14. Enter Disk space you want to allocate for "EFI System Partition (ESP)".
    <br>
          <img width="452" height="110" alt="image" src="https://github.com/user-attachments/assets/4efa2480-0091-4505-be46-36ad75e4903c" /><br><br>
15. Enter Disk space you want to allocate for "EXtended Bootloader Partition (XBOOTLDR)".
    <br>
          <img width="452" height="107" alt="image" src="https://github.com/user-attachments/assets/b731ceca-4f15-4a26-bd6c-105ef1710f6a" /><br><br>
16. Enter Disk space you want to allocate for "SWAP".
    <br>
          <img width="454" height="105" alt="Screenshot 2025-11-03 at 12 16 07 AM" src="https://github.com/user-attachments/assets/2a8abbf0-9e69-4607-896d-3acac470b313" /><br><br>
17. Select "ext4 Ext4" in Filesystem and home
    <br>
          <img width="315" height="138" alt="image" src="https://github.com/user-attachments/assets/21848b03-4f2f-4694-a7c8-e9beda4e841b" /><br><br>
18. Confirm the file system you want to use.
19. Allocate your disk space for _/home_ directory
20. Confirm it!
21. Authorize the deletion of ALL DATA in on _/dev/sda_
    <br><br>
          <img width="315" height="138" alt="image" src="https://github.com/user-attachments/assets/59efa294-2ae6-4fe5-9147-34c24557af97" />



