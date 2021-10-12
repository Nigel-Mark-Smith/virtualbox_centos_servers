# virtualbox_centos_servers

This repository details procedures for creating and configuring
CentOS VirtualBox VM's. The procedures make use of the 
'VBoxManage' command line utility to create, manipulate and remove VM's
and are intended to be exceuted in the order detailed below building a server
network capable of supporting PXE installation, LDAP authentication and
provding iSCSI backend storage. Where detailed the names of the DVD ISO image 
(CentOS-7-x86_64-Everything-2009.iso) and the bridgeadapter<x> values 
('Realtek PCIe GBE Family Controller' and 'Intel(R) Gigabit ET Dual Port 
Server Adapter') should be replaced by the requisite values returned by 
the following on your host PC.

- 'VBoxManage list --long dvds'
- 'VBoxManage list --long bridgedifs'

To execute all processes detailed requires that the following are true.

- Oracle VM VirtualBox is installed on the host PC.
- A binary image of the CentOS DVD installation image (ISO) is 
  available in the Oracle VM VirtualBox installation.
- Two physical NIC cards are installed on the host PC.
- All VM's can be defined in subfolders of X:\VM or Y:\VM ( see
  'VBoxManage setproperty machinefolder...' ).

See the following links for further details of obtaining this software:

https://www.centos.org/

https://www.virtualbox.org/

It is also recommended that Putty is installed on the host PC.
This can be downloaded from the following link:

https://www.putty.org/


Document File|File Contents|Execution order
-------------|-------------|---------------
Manual_Installation_of_CentOS_on_a_VirtualBox_VM.docx|Steps for installing CentOS manually on VM|N/A
Installation_of_FreeIPA_VirtualBox_VM.docx|Steps for installing FreeIPA software using script 'ipa-server-install'|N/A
Create_dummy_server.txt|Creating VirtualBox VM|1
Create_an_installation_drive.txt|Creating a CentOS installation disk|2
Create_an_installation_clone.txt|Creating a template CentOS VM|3
Create_DHCP_server.txt|Creating a new server (DHCP) using template VM|4
Complete_DHCP_server_configuration.txt|Completing configuration of DHCP server|5
Create_a_web_server.txt|Creating a web server|6
Create_new_server_using_PXE.txt|Creating a new server using PXE|7
Create_authentication_server|Creating an LDAP authentication server|8
Create_server_test_using_PXE|Creating a new server with a fixed IP address using PXE|9
Create_iSCSI_target_server|Creating a new server which provides iSCSI backend storage|10
Create_iSCSI_initiator_server|Creating a new server which utilises iSCSI backend storage|11
Create_router_server|Creating a new server which can route IP traffic|12
APPENDIX_A.txt|Template for removal of a VM|N/A
APPENDIX_B.txt|Process for installing Guest Additions on VM|N/A
EnablingSSHonPC.txt|Steps for installing an open SSH server on a Windows 10 PC|N/A




