# IT Support Network Project

## Table of Contents
1. [Project Overview](#project-overview)
2. [Architecture](#architecture)


## Project Overview 

This project simulates an enterprise network environment using Windows virtual machines.

## Architecture
The network will comprise of the following components

- **Domain Controller (DC)**: A windows Server 2022 VM that handles Active Directory, DNS, and DHCP services. 
- **Client Machines**: Multiple Windows 10 VMs representing end-user workstations.
- **File Server**: A dedicated VM for file storage and sharing.
- **Web Server**: A VM running IIS to host internal web applications.
- **Print Server (Optional)**: A VM to manage print jobs. 

1. **Create Virtual Machines**
	- Go to [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/) and download Windows 10 Enterprise and Windows Server 2022.  
	- Create 3 Windows Server 2022 VMs, 1 Domain Controller, 1 File Server and 1 Web server. 
	- Create multiple Windows 10 VMs for client machines. 
	
2. **Install Active Directory**
	- On one Windows Server 2022 VM install Active Directory Services role and promote the server to a Domain Controller.

3. **Configure DNS and DHCP**
	-  Set up DNS to resolve domain names and DHCP to assign client machines.

4. **Set Up File Server and Web server**
 - Install file server and web server roles on separate VMs.
 

## Services
### Domain Controller
- Handles user authentication and authorization.
- Manages DNS and DHCP services.

### File Server
- Provides shared storage for users.
- Configured with NTFS permissions for access control.

### Web Server
- Hosts internal applications and resources.
- Accessible via the internal network.

### Print Server
- Manages print jobs from client machines.

## Troubleshooting
Common issues and solutions:
- **Issue**: Client machines cannot connect to the Domain Controller.
  - **Solution**: Check network connectivity and ensure the DC is running.

- **Issue**: DNS resolution fails.
  - **Solution**: Verify DNS settings on the client machines.

## User Guide
Instructions for users on how to interact with the network:
- Access shared files on the File Server.
- Use internal applications hosted on the Web Server.
- Print documents via the Print Server.

## Contributing
If you would like to contribute to this project, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


### Useful Links
1. [How to create a Virtual machine using Hyper-V](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/create-virtual-machine)