+++
date = '2025-08-29T09:48:20+01:00'
draft = false
layout = "simple"
title = 'Map Network Drive'
+++
## Overview
The acquisition computer filesystem is meant for *temporary* storage of data acquired by the microscopes. Part of the imaging workflow --- after acquisition --- is to manage your data. Initially this means you must move the data somewhere for permanent storage, archiving and backup. To achieve this on our acquisition systems, you mount a network share as a local drive during your session. This allows you to drag and drop your files from the local computer's hard disk drive to the network computer's hard disk drove. The process of adding a network shared drive to a local system is known as "mapping a network drive". The following instructions describe one way to mount network shared drives on microscope acquisition systems. Our acquisition systems use *Windows* as the operating system.
### Prerequisites
To mount a network shared drive, you must have access to a network shared drive (obviously). At King's, institutionally provided data storage is managed through [*King's Computational Research, Engineering and Technology Environment*](https://er.kcl.ac.uk). To request access, please fill in the form linked at [this](https://docs.er.kcl.ac.uk/research_data/rds_requesting_access/) website.
<details>
  <summary>{{< icon "microsoft" >}} Windows</summary>

### The Procedure
There are several ways to successfully mount a network location as a local drive so that you can copy your data to the network drive and then delete it from the local drive. The following method uses the Windows GUI.

#### Step by Step
{{< columns >}}  
1. Select 'This Computer' in the navigation pane of an explorer window.
1. Right-click on the computer icon, revealing the contextual menu.
1. Select "Map Network Drive" from the contextual menu.
1. The drive letter can be anything that is not currently in use.
1. in the "Folder" field, enter the path to your RDS share, starting with two backslashes. At acquisition and analysis workstations, be sure to add the "hsrn" between the rds and the er portions of the address, this ensures your data travels across the <u>h</u>igh <u>s</u>peed <u>r</u>esearch <u>n</u>etwork. Leave out the "hsrn" from the string when using another computer in your lab. 

    ---
    - e.g. ***\\\rds.hsrn.er.kcl.ac.uk\prj\dn_cdn_microscopy***
    - This would be my path from an acquisition system.

    ---
    - ***\\\rds.er.kcl.ac.uk\prj\dn_cdn_microsocpy***
    - This would be my path from a non-acquisition Windows system.
    ---
1. Make sure the "Connect using different credentials" tickbox *is* ticked and the "Reconnect at sign-in *is* ***NOT*** ticked.
1. In this context, "different credentials" means different to the ones used to login to the local acquisition computer. 
1. Click "Finish". This will cause a pop-up window to appear where you can add your credentials.

{{< column >}}
{{< figure
    src="mapNetworkDrive1.png"
    default=true
    height="50px"
    >}}
 ----
{{< figure
    src="mapNetworkDrive.png"
    default=true
    height="50px"
    >}}
{{< endcolumns >}}
----
#### Authenticate
{{< columns >}}
1. Depending on the verion of Windows you are using, this window may differ significantly.
2. Enter your user name in the user field in the format: KCLAD\k########
3. Enter your password in the password field, press "OK".
4. If everything is entered correctly and the moon is in the right phase, then your folder on RDS will appear in an explorer window.
5. You can now treat the RDS space as if it's a local drive and drag and drop your image data to your RDS space.
6. Shutting down or logging out of the system will automatically disconnect your RDS space. You can also right click on the drive and "disconnect" to ensure that the next person using the microscope will not be able to add/delete data in your space. 
{{< column >}}
{{< figure
    src="credentials.png"
    default=true
    height="50px"
    >}}
{{< endcolumns >}}  
</details>

<details>
  <summary>{{< icon "apple" >}} MacOS</summary>
  
#### Step By Step
{{< columns >}}
1. With the finder active, click on ⌘+K to bring up the "Connect to Server" dialogue box.
1. Enter the path to your RDS share in the "Server Address:" field, starting with "smb://"

{{< alert cardColor=#3b82f6 >}}
None of our acquisition computers runs MacOS, so you will always connect to your RDS using the following format:
{{< /alert >}}
    - e.g. ***smb://rds.kcl.ac.uk/prj/dn_cdn_microsocpy***
    
1. Click "Connect" to initialise the connection, which initiates the authentication process.
1. When the authentication window appears, enter your credentials in the following format:
    - Username: DOMAIN\username --- i.e. KCLAD/k###########
    - Password: Your password for that account.
1. The RDS share should appear as a connected network shared drive.
1. You can now treat the RDS space as if it's a local drive and drag and drop your image data to your RDS space.
1. Shutting down or logging out of the system will automatically disconnect your RDS space. If you're using a communal computer you can also right click on the drive and select "eject" to ensure that the next person using the computer will not be able to add/delete your data.
1. MacOS stupidly remembers the credentials of the first person to connect to a shared drive and reuses these to connect subsequently. The only way to get the computer to forget the credentials and login to the server with different credentials is to restart.
{{< column >}}
{{< figure
    src="MacOSConnectToServer.png"
    default=true
    height="50px"
    >}}
{{< figure
    src="MacOSConnect2.png"
    default=true
    height="50px"
    >}}
{{< endcolumns >}} 
{{< columns >}}
{{< figure
    src="Connect3.png"
    default=true
    height="50px"
    >}}
    {{< column >}}
{{< figure
    src="authenticate.png"
    default=true
    height="50px"
    >}}
{{< endcolumns >}}  
</details>

 <details>
 <summary>{{< icon "ubuntu" >}} Linux</summary>

1. Open the Files application.
{{< figure
    src="linux/files-launch.png"
    default=true
    height="50px"
    >}}
1. Navigate to the “Other Locations” section from the sidebar menu.
{{< figure
    src="linux/files-main.png"
    default=true
    height="50px"
    >}}
1. Locate the network hosts under the “Networks” section or enter the host's IP address with the smb: prefix and click Connect.
1. Enter the shared drive path in the following format:
    - ***smb://rds.kcl.ac.uk/prj/dn_cdn_microsocpy***
{{< figure
    src="linux/files-other-locations.png"
    default=true
    height="50px"
    >}}
1. Choose the shared folder you wish to access.
{{< figure
    src="linux/files-other-locations-folders.png"
    default=true
    height="50px"
    >}}
1. Select “Connect” with Registered User selected. Enter login credentials and click Connect.
    - Username = your username
    - DOMAIN = KCLAD
    - Password = your password

{{< figure
    src="linux/files-other-locations-folders-authenticate-registered.png"
    default=true
    height="50px"
    >}}
1. Access the files and folders provided by the remote host.

1. Unmount the shared folder by clicking the eject icon when finished.
{{< figure
    src="linux/files-other-locations-folders-unmount.png"
    default=true
    height="50px"
    >}}
</details>
