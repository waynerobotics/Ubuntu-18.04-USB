# Ubuntu-18.04-USB

**Simple instructions on how to run Ubuntu 18.04 off a USB drive. No need for dual-booting anymore!** 

***Courtesy of [@LuayJ](https://github.com/LuayJ)***

## Things you'll need:
* A VM (I used Oracle VM VirtualBox)
* An ISO image of Ubuntu 18.04 Desktop
* A USB drive (at least 16 GB)

## Steps:
1. **Create a VM**
    1. Type: Linux
    2. Version: Ubuntu 64-bit (this should match the ISO file)
    3. Memory size: doesn't really matter
    4. Hard disk: you should be able to do this without setting up a hard disk of any sort
    5. Click create


2. **You should now see it on the LH side under whatever you named it**
    1. Click on it and go to its settings --> storage
    2. In storage, under devices you should see "Controller: IDE", click on it
    3. Next to "Controller: IDE" 2 things should show up: "Adds Optical Drive" and "Adds Hard Disk"
    4. Click "Adds Optical Drive", the ISO file might be in the submenu that pops up or it might not
        1. If its not, click "Add Disk Image" and find it then click choose and OK
    5. You should see "Storage IDE Primary Master" as the ISO image you chose on the main menu RH side

3. **Start the VM (it might take a bit, but it'll load)**
    1. Click TRY Ubuntu when that menu pops up and wait for it to load
    2. You should be on the Ubuntu Desktop by now, and there should be an "Install Ubuntu 18.04" on the desktop as well
    3. Plug in your drive and make sure the VM can see it (you may have to tinker with the Devices menu)
        1. Please make sure you didn't accidentally add your HDD or SSD or any other drive here
    4. Open GParted and make sure its there again (note what its called e.g. sdb or whatnot and the filesystem)
    5. Open the "Install Ubuntu" thing
    6. Once you get to the Installation Type page, click Something Else
    7. On the next page, find your flash drive (should be the only thing showing up really)
        1. It should have a type of ext4
            1. Choose the main one, not the one with that says the type next to it (a small indentation should let you know which is which)
        2. On the "Device for boot loader installation" drop down menu, also choose the USB drive
    8. Click "Install Now"

***When booting up you'll need to change from UEFI to Legacy BIOS in that menu to use the drive, then back to UEFI to use windows***
