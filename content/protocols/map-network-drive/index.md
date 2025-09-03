+++
date = '2025-08-29T09:48:20+01:00'
draft = false
layout = "simple"
title = 'Map Network Drive'
+++

## Overview
The acquisition computer filesystem is meant for *temporary* storage of data acquired by the microscopes. Part of the imaging workflow --- after acquisition --- is to manage your data. Initially this means you must move the data somewhere for permanent storage, archiving and backup. To achieve this on our acquisition systems, you mount a network share as a local drive during your session. This allows you to drag and drop your files from the local computer's hard disk drive to the network computer's hard disk drove. The process of adding a network shared drive to a local system is known as "mapping a network drive". The following instructions describe one way to mount network shared drives on microscope acquisition systems. Our systems use *Windows* as the operating system. These instructions are specific for Windows.

### Prerequisites
To mount a network shared drive, you must have access to a network shared drive (obviously). At King's, institutionally provided data storage is managed through [*King's Computational Research, Engineering and Technology Environment*](https://er.kcl.ac.uk). To request access, please fill in the form linked at [this](https://docs.er.kcl.ac.uk/research_data/rds_requesting_access/) website.

### The Procedure
There are several ways to successfully mount a network location as a local drive so that you can copy your data to the network drive and then delete it from the local drive. The following method uses the Windows GUI.  
1. Select 'This Computer' in the navigation pane of an explorer window.
2. Right-click on the computer icon, revealing the contextual menu.
3. Select "Map Network Drive" from the contextual menu.
4. 
{{< figure
    src="mapNetworkDrive.png"
    default=true
    height="50px"
    >}}