+++
title = 'Map a Network Drive (RDS)'
layout = "simple"
+++

## Why this matters

The acquisition computers store data **temporarily**. Copy your data to King's Research Data Storage (RDS) after every session. Then delete it from the acquisition computer **after checking the copy**.

You do this by connecting ("mapping") your RDS folder as a drive for the duration of your session.

## Before you start

You need an RDS project folder. If you don't have one:

{{< alert icon="play" cardColor=#3b82f6 >}}[Request RDS from Advanced REsearch Computing](https://rds-admin.er.kcl.ac.uk/){{< /alert >}}

You also need your k-number and King's password.

## Which address do I use?

| You are on... | Address format |
|---|---|
| A facility **acquisition or analysis** computer (Windows) | `\\rds.hsrn.er.kcl.ac.uk\prj\<your_project>` (high-speed research network) |
| Any other Windows computer | `\\rds.er.kcl.ac.uk\prj\<your_project>` |
| macOS or Linux | `smb://rds.er.kcl.ac.uk/prj/<your_project>` |

Example project: `dn_cdn_microscopy`. Off campus or on Wi-Fi, you may first need a VPN ([e-Research OpenVPN guide](https://docs.er.kcl.ac.uk/CREATE/tools/openvpn/)).

## Windows

1. Open File Explorer and select **This PC**.
2. Right-click **This PC** and choose **Map network drive**.
3. Choose any unused drive letter.
4. In **Folder**, type your address from the table above.
5. Tick **Connect using different credentials**.
6. **Untick Reconnect at sign-in.**
7. Click **Finish**.
8. Enter your username as `KCLAD\k1234567` (your own k-number) and your password.
9. **Untick "Remember my credentials"** if shown.
10. Your RDS folder opens. Copy your files across.

{{< figure src="mapNetworkDrive1.png" default=true width="300" >}}
{{< figure src="mapNetworkDrive.png" default=true width="300" >}}
{{< figure src="credentials.png" default=true width=300 >}}

### When you finish

1. Check the copied files open and the sizes match.
2. Delete your data from the acquisition computer.
3. Right-click the drive and choose **Disconnect**. Logging out also disconnects, but do it yourself so the next user cannot reach your data.

### It didn't connect?

- Check the address for typos and the `hsrn` part.
- Check you used `KCLAD\` before your k-number.
- Confirm your RDS access has been approved.
- Still stuck? Email [the facility manager](mailto:stephen.ogg@kcl.ac.uk).

## macOS

You are using your own computer, so use the `rds.er` address.

1. In Finder, press <kbd>⌘</kbd>+<kbd>K</kbd>.
2. Enter the `smb://` address and click **Connect**.
3. Enter `KCLAD\k1234567` and your password.
4. Drag and drop your files into the share.
5. When finished, eject the drive.

macOS remembers the first account used. To connect as a different user, use `smb://new_username:*@server_address/share_name`.

{{< figure src="MacOSConnectToServer.png" default=true height="50px" >}}
{{< figure src="authenticate.png" default=true height="50px" >}}

## Linux

1. Open **Files**, then **Other Locations**.
2. In **Connect to Server**, enter the `smb://` address.
3. Choose **Registered User**; set Username to your k-number, Domain to `KCLAD`, and enter your password.
4. Copy your files, then unmount with the eject icon.

{{< figure src="linux/files-other-locations.png" default=true height="50px" >}}
