# Windows 10 Workstation

## Overview

A Windows 10 virtual workstation was deployed and integrated into the Active Directory environment to simulate an enterprise endpoint.

The workstation is connected to the pfSense GREEN internal network and joined to the `soc.lab` Active Directory domain.

## Lab Configuration

| Configuration | Value |
|---|---|
| Hostname | SOC-Win10 |
| Operating System | Windows 10 |
| IP Address | 192.168.1.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.1.1 |
| DNS Server | 192.168.1.10 |
| Domain | soc.lab |
| NetBIOS Domain | SOC |
| Virtualization | Oracle VirtualBox |

## Network Configuration

The workstation was connected to the `GREEN` Internal Network in VirtualBox.

Static IPv4 configuration:

```text
IP Address:      192.168.1.20
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.1.1
Preferred DNS:   192.168.1.10
