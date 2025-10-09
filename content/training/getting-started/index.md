+++
title= "Getting Started"
layout = "simple"
+++

## Overview
Getting started imaging with our resources requires:
- **An account in Stratocore PPMS** --- for booking and billing.
- **Training** --- so that you don't damage the equipment or yourself.
- **Physical Access** --- so that you can get into the rooms where the microscopes live.
- **A strategy to manage your image data** --- to keep our acquisition computers from filling up with data and as a means for you to have access to your data.

## PPMS
Stratocore [PPMS](https://stratocore.com/), our booking and billing system, is a cloud-based management software designed for scientific core facilities and research labs, providing a centralized platform for equipment booking, training, maintenance, billing, and project tracking. The system supports various functions, from managing access to advanced resources to simplifying financial operations and ensuring compliance for researchers and facility staff.
To use *many* of the shared resource facilities at KCL, you will need an account in the system.
To access the King's instance of PPMS, please visit this URL: [https://ppms.eu/kcl](https://ppms.eu/kcl). This is the landing page for all the facilities that use PPMS at KCL. Click on the link to the CDN facility to reach our facility and login with your k-number.
### PPMS Booking Policies
- You may book 1 week in advance
- Booking will open at 11:00 on Thursday for the following Monday to Sunday period.
- Each day, from 08:00 – 20:00, is split into 6 x 2-hour booking slots – bookable sessions are for a minimum of 2 hours. If you straddle two slots **YOU WILL BE CHARGED FOR BOTH**. 
- Each approved user is entitled to 6 hours (3 x 2-hour sessions) on the scope per week plus one overnight session (from Monday to Friday). You can additionally book a further 4 hours and one overnight session at the weekend if needed and is on a first-come, first-served basis.
 - If you have already used your weekly allowance, you can book extra slots, but only if there are available slots on the day. 
- Cancellation within 24h of the start of hte booking will incur a charge.
## Training
To use any system by yourself, you will require training. Please wait to request training until you have some samples to image. Bring your samples to the training session so that we can use them to personalize your training.  
To organise training, login to PPMS, and then fill in the ["CDN Microscope Training Request Form"](https://ppms.eu/kcl/req/?pf=4&training=true&form=11) you can find in the *Requests* tab. Once the form is submitted, I will contact you to ask for further details or to arrange a mutually agreeable time for the taining. Training sessions last approximately 1.5h to 2h. After the training, you will be granted access to the booking calendar for that system. 

## Physical Access
Your ID card can be programmed to allow you into the centre and into the microscope room. After the training, email to the [CDN Technical Services](mailto:cdn-technical-services@kcl.ac.uk) team to request access. Copy [me](mailto:stephen.ogg@kcl.ac.uk) so they know that I have given you the appropriate training. 

## Data Management
An important part of an imaging experiment is data management. Initially acquired image data are saved on the filesystem of the local computer that is directly connected to the microscope. These computers have limited data storage capacity. They have room to store acquired data for ~1 week to 1 month. This estimate is *highly* dependent on the schedule of the specific system. As an upstanding imaging citizen, it is **your** job to transfer your data off the acquisition system, moving it to a location for long-term storage, backup, analysis, and archiving. The *only* way to do this is over the newtork. USB ports have been disabled in the BIOS, preventing users from plugging in USB storage devices to copy their data. This is to prevent any inadvertent transfer of viruses to the acquisition systems.  
I will not delete your data from the acquisition system for no reason. If someone needs space to acquire their data, however, I will delete data until there is enough space for new data to be acquired. I´ll delete oldest data first, but *without any warning* or notification. This is so important it bears repeating -- **YOU ARE RESPONSIBLE FOR YOUR OWN DATA!!** Please see [this](/protocols/map-network-drive) page to start using a strategy that is implemented by the [e-Research](https://docs.er.kcl.ac.uk/) group at King´s called [RDS](https://docs.er.kcl.ac.uk/research_data/rds/)---Research Data Storage.
{{< columns >}}
{{< alert icon="play" cardColor=#3b82f6 >}}[Request RDS from e-Research](https://rds-admin.er.kcl.ac.uk/){{< /alert >}}
{{< column >}}
{{< endcolumns >}}