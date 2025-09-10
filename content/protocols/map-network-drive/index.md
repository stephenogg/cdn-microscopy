+++
date = '2025-08-29T09:48:20+01:00'
draft = false
layout = "simple"
title = 'Map Network Drive'
+++
## Overview
The acquisition computer filesystem is meant for *temporary* storage of data acquired by the microscopes. Part of the imaging workflow --- after acquisition --- is to manage your data. Initially this means you must move the data somewhere for permanent storage, archiving and backup. To achieve this on our acquisition systems, you mount a network share as a local drive during your session. This allows you to drag and drop your files from the local computer's hard disk drive to the network computer's hard disk drove. The process of adding a network shared drive to a local system is known as "mapping a network drive". The following instructions describe one way to mount network shared drives on microscope acquisition systems. Our systems use *Windows* as the operating system. The procedure below works for Windows

### Prerequisites
To mount a network shared drive, you must have access to a network shared drive (obviously). At King's, institutionally provided data storage is managed through [*King's Computational Research, Engineering and Technology Environment*](https://er.kcl.ac.uk). To request access, please fill in the form linked at [this](https://docs.er.kcl.ac.uk/research_data/rds_requesting_access/) website.

### The Procedure
There are several ways to successfully mount a network location as a local drive so that you can copy your data to the network drive and then delete it from the local drive. The following method uses the Windows GUI.
#### TL;DR
{{< columns >}}  
1. Select 'This Computer' in the navigation pane of an explorer window.
2. Right-click on the computer icon, revealing the contextual menu.
3. Select "Map Network Drive" from the contextual menu.
4. in the "Folder" field, enter the path to your RDS share, starting with two backslashes. At acquisition and analysis workstations, be sure to add the "hsrn" between the rds and the er portions of the address, this ensures your data travels across the <u>h</u>igh <u>s</u>peed <u>r</u>esearch <u>n</u>etwork. Leave out the "hsrn" from the string when using another computer in your lab. 
    - e.g. ***\\\rds.hsrn.er.kcl.ac.uk\prj\dn_cdn_microscopy***
5. Make sure the "Connect using different credentials" tickbox *is* ticked and the "Reconnect at sign-in *is* ***NOT*** ticked.
6. Click "Finish". This will cause a pop-up window to appear where you can add your credentials.
{{< column >}}
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
{{< column >}}
{{< figure
    src="credentials.png"
    default=true
    height="50px"
    >}}
{{< endcolumns >}}