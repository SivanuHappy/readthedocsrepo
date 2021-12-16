Virtual Ubuntu environment via VirtualBox
=========================================

VirtualBox is a tool which allows you to run different operating systems virtually on your host operating system. This is referred to as a virtual machine.

Install VirtualBox
---------------------

1. In order to install VirtualBox, follow this (you can `register for a free account <https://github.com/signup>`_ if you don't have one).
2. Under “VirtualBox 6.1.28 platform packages”, select the Windows host download link.
3. Open VirtualBox.

Download Ubuntu ISO file
------------------------------------

1. For the purposes of this document I will be utilizing Ubuntu 20.04, although 18.04 is recommended.
2. Follow this link.
3. Under the "Download" button select "20.04 LTS".

Set Up Ubuntu virtual machine in VirtualBox
--------------------------------------------
1. Open VirtualBox.
2. Click the "New" button.
3. Provide the name of your new machine (I recommend the name Ubuntu 20.04).
4. Set Machine folder location (your choice).
5. Ensure the Type and version fields are correct (Type: Linux ; Version: Ubuntu (64-bit)).
6. Select "Next".
7. Select memory size (Anywhere inside the green area of the scale).
8. Select "Next".
9. Select “Create a virtual hard disk now”.
10. Select "Create".
11. Select "VDI" (Virtual Disk Image).
12. Select "Next".
13. Select "Dynamically Allocated" (Allows the OS to expand disk size if required).
14. Select "Next".
15. Choose "File Location".
16. Choose virtual hard disk size (I recommend around 100GB).
17. Click "Create".

Configure Settings for Ubuntu virtual Machine
----------------------------------------------
1. Select your machine.
2. Select "Settings".
3. Under "General", click "Advanced Settings". Select "Bidirectional" for both shared clipboard and drag and drop fields. This will allow you to share files between host machine and Ubuntu machine.
4. Under "System", click "processor". Choose the number of CPUs you wish to use (if no preference leave as default).
5. Under "Storage", click "Empty". Under "Attributes", by optical drive click Disk dropdown and choose a disk file. Provide location for ISO file downloaded in step 2.
6. Select "OK".

Open your virtual machine
-------------------------------------
1. Select your machine and press start.
2. Select preferred language and click "Install Ubuntu".
3. Select "Keyboard Layout and Language", click "Continue".
4. Under “What apps would you like to start with?”, select "Normal installation".
5. Under “Other Options”, select download updates while installing Ubuntu. Then install third party software for graphics and Wi-Fi hardware, and additional media formats.
6. Click "Continue".
7. Under "Installation Type", select "Erase Disk and install Ubuntu".
8. Click "Install Now".
9. Click "Continue".
10. Select your location.
11. Enter your preferred name, "Username" and "Password".
12. Click "Continue".
13. Wait for installation to complete.
14. Click "Restart Now".
15. Log in to the user that you created.
16. Follow Setup Instructions provided by the OS.

(Optional) Install VirtualBox Guest Additions
------------------------------------------------------
This software will allow your VirtualBox virtual machine to properly maximize on your screen.

1. Open Terminal.
2. Give command: sudo apt install build-essential dkms linux-headers-$(uname -r).
3. Provide your password.
4. Enter "y", press enter.
5. Close Terminal.
6. Select "devices" on VirtualBox window.
7. Select "Insert Guest additions CD Image".
8. Select "Run".
9. Provide your password, click "Authenticate".
10. Restart Ubuntu operating system.

