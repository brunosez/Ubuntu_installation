# Ubuntu_installation
Note on Ubuntu installations

Some hints to install Ubuntu in a fresh Dell XPS machine, with win10 pre-installed

Bios setup is accessible by pressing F12 in the boot sequence

Main issues are :

* Switch to **AHCI mode** for the Disk Drive

You can follow <http://triplescomputers.com/blog/uncategorized/solution-switch-windows-10-from-raidide-to-ahci-operation/>

Mainly put in safe mode , swith to AHCI , this will install the correct drivers, and cancel the safe mode boot

* **Install by hand** the Artheros wifi card drivers !!

This is explained here , you must get the drivers here 

<https://github.com/kvalo/ath10k-firmware/tree/master/QCA6174>

exact hw number and package can differ

sudo rm -r /lib/firmware/ath10k
sudo cp -r ath10k-firmware/ /lib/firmware/ath10k/
sudo mv /lib/firmware/ath10k/QCA6174/hw3.0/firmware-5.bin_SW_RM.1.1.1-00157-QCARMSWPZ-1 /lib/firmware/ath10k/QCA6174/hw3.0/firmware-5.bin

