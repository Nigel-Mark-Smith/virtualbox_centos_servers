# virtualbox_centos_servers

This repository details procedures for creating and configuring
CentOS VirtualBox VM's. The procedures make use of the 
'VBoxManage' command line utility to create, manipulate and remove VM's
and are intended to be exceuted in the order detailed below building a server
network capable of supporting PXE installation. Where detailed the names
of the DVD ISO image (CentOS-7-x86_64-Everything-1908.iso) and the 
bridgeadapter<x> values ('Realtek PCIe GBE Family Controller' and
'Intel(R) Gigabit ET Dual Port Server Adapter') should be replaced by
the requisite values returned by the following on your host PC.

- 'VBoxManage list --long dvds'
- 'VBoxManage list --long bridgedifs'

To execute all process detailed requires that the following are true.

- Oracle VM VirtualBox is installed on the (Guest) PC.
- A binary image of the CentOS DVD installation image (ISO) is 
  available in the Oracle VM VirtualBox installation.
- Two physical NIC cards are installed on the host PC.
- All VM's a defined in subfolders of X:\VM ( see
  'VBoxManage setproperty machinefolder' ).

See the following links for further details of obtaining this software:

https://www.centos.org/
https://www.virtualbox.org/

It is also recommended that Putty is installed on the host PC
this can be downloaded from the following link:

https://www.putty.org/


Document File|File Contents|Execution order
-------------|-------------|---------------
Manual_Installation_of_CentOS_on_a_VirtualBox_VM.docx|Steps for installing CentOS manually on VM|N/A
Create_dummy_server.txt|Creating VirtualBox VM|1
Create_an_installation_drive.txt|Creating a CentOS installation disk|2
Create_an_installation_clone.txt|Creating a template CentOS VM|3
Create_new_server.txt|Creating a new server (DHCP) using template VM|3
Complete_DHCP_server_configuration.txt|Completing configuration of DHCP server|4
Create_a_web_server.txt|Creatind a web server|5
Create_new_server_using_PXE.txt|Creating a new server use PXE|6
APPENDIX_A.txt|Template for removal of a VM|N/A
APPENDIX_B.txt|Process for install Guest Additions on VM|N/A



