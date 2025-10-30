+++
date = '2025-08-29T09:48:20+01:00'
draft = false
layout = "simple"
title = 'Map Network Drive'
+++
## Overview
The acquisition computer filesystem is meant for *temporary* storage of data acquired by the microscopes. Part of the imaging workflow --- after acquisition --- is to manage your data. Initially this means you must move the data somewhere for permanent storage, archiving and backup. To achieve this on our acquisition systems, you mount a network share as a local drive during your session. This allows you to drag and drop your files from the local computer's hard disk drive to the network computer's hard disk drove. The process of adding a network shared drive to a local system is known as "mapping a network drive". The following instructions describe one way to mount network shared drives on microscope acquisition systems. Our acquisition systems use *Windows* as the operating system.
### Prerequisites
To mount a network shared drive, you must have access to a network shared drive (obviously). At King's, institutionally provided data storage is managed through [*King's Computational Research, Engineering and Technology Environment*](https://er.kcl.ac.uk).
{{< alert icon="play" cardColor=#3b82f6 >}}[Request RDS from e-Research](https://docs.er.kcl.ac.uk/research_data/rds_requesting_access/){{< /alert >}}

<details>
  <summary>{{< icon "microsoft" >}} Windows</summary>

### The Procedure
There are several ways to successfully mount a network location as a local drive so that you can copy your data to the network drive and then delete it from the local drive. The following method uses the Windows GUI.

{{< timeline >}}
{{< timelineItem icon="1" md="true" >}}
Select 'This Computer' in the navigation pane of an explorer window.
{{< /timelineItem >}}
{{< timelineItem icon="2" >}}
Right-click on the computer icon, revealing the contextual menu.
{{< /timelineItem >}}
{{< timelineItem icon="3" >}}
Select "Map Network Drive" from the contextual menu.
{{< figure
    src="mapNetworkDrive1.png"
    default=true
    width="300"
    >}}
{{< /timelineItem >}}
{{< timelineItem icon="4" >}}
 This will cause a new pane to open, asking for information about how to map the network drive.
 <ul>
 <li>The drive letter can be anything that is not currently in use.</li>
 <li>In the "Folder" field, enter the path to your RDS share, starting with two backslashes. At acquisition and analysis workstations, be sure to add the "hsrn" between the rds and the er portions of the address, this ensures your data travels across the <u>h</u>igh <u>s</u>peed <u>r</u>esearch <u>n</u>etwork. Leave out the "hsrn" from the string when using another computer in your lab.</li> 
<li>Make sure the "Connect using different credentials" tickbox <i>is</i> ticked and the "Reconnect at sign-in <em>is</em> <em><strong>NOT</strong></em> ticked.</li>
<li>In this context, "different credentials" means different to the ones used to login to the local acquisition computer.
</li>
<li>e.g.
    <ul>
    <li><i>\\rds.hsrn.er.kcl.ac.uk\prj\dn_cdn_microscopy</i> Would be my path from an acquisition system.</li>
    <li><i>\\rds.er.kcl.ac.uk\prj\dn_cdn_microscopy</i> would be my path from any other non-acquisition system.</li>
    </ul>
</li>
<li>Clicking "Finish" will cause a pop-up window to appear where you can add your credentials.</li>
</ul>
{{< figure
    src="mapNetworkDrive.png"
    default=true
    width="300"
    >}}
{{< /timelineItem >}}
{{< /timeline >}}


{{< timeline >}}
{{< timelineItem icon="5" subheader="Authenticate" >}}
Depending on the verion of Windows you are using, this window may differ significantly.
<ul>
<li>Enter your user name in the user field in the format: KCLAD\k########</li>
<li>Enter your password in the password field, press "OK".</li>
</ul>

If everything is entered correctly and the moon is in the right phase, then your folder on RDS will appear in an explorer window. You can now treat the RDS space as if it's a local drive and drag and drop your image data to your RDS space. Shutting down or logging out of the system will automatically disconnect your RDS space. You can also right click on the drive and "disconnect" to ensure that the next person using the microscope will not be able to add/delete data in your space. 

{{< figure
    src="credentials.png"
    default=true
    width=300
    >}}

{{< /timelineItem >}}
{{< /timeline >}}

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