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

### Static IPv4 configuration:


IP Address:      192.168.1.20
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.1.1
Preferred DNS:   192.168.1.10

The Active Directory server was configured as the primary DNS server because domain services depend on Active Directory-integrated DNS.

### Connectivity Testing

Connectivity was verified between the workstation, pfSense gateway and Active Directory server.

ping 192.168.1.1
ping 192.168.1.10
ping 8.8.8.8

DNS resolution was also tested:

nslookup google.com
Active Directory Domain Join

The Windows 10 workstation was successfully joined to:

Domain: soc.lab
NetBIOS: SOC

The workstation was then restarted to complete the domain join.

Domain Authentication

Domain authentication was verified using the Active Directory Administrator account.

### SOC\Administrator

The logged-in identity was verified using:

whoami

### Expected result:

soc\administrator
Purpose in the SOC Lab

The Windows 10 workstation acts as the primary endpoint used for security monitoring and investigation.

It provides a controlled environment for generating endpoint activity such as:

Process creation
Process termination
DNS queries
User authentication
File activity
PowerShell activity
Network connections
Suspicious endpoint behavior

Sysmon was subsequently deployed on this workstation to provide enhanced endpoint telemetry for SOC investigations.
