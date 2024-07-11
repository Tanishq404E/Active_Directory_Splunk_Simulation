# Active Directory and Splunk Simulation using Kali Linux as Attack Box

## Project Overview
This project involves setting up a simulated Active Directory environment with integrated Splunk monitoring and sysmon to gather logs. The setup includes multiple virtual machines (VMs) to mimic a real-world enterprise network. The project showcases how to monitor and analyze security events using Splunk, with Kali Linux serving as the attack box to simulate various attack scenarios.

## Flowchart
![Active Directory](https://github.com/Tanishq404E/Active_Directory_Splunk_Simulation/assets/70007965/eaacb637-82f4-4d32-9066-4ba505445c43)


## Project Components
1. **Active Directory Server**:
   - **OS**: Windows Server 2022
   - **Users**: Raven Fury, John Doe
   - **Roles**: Active Directory Domain Services, DNS

2. **Windows 10 Pro Client**:
   - **OS**: Windows 10 Pro
   - **User**: Raven Fury
   - **Features**: Remote Desktop Protocol (RDP) enabled

3. **Splunk Server**:
   - **OS**: Ubuntu Server 22.04
   - **Installed Software**: Splunk Enterprise

4. **Kali Linux Attack Box**:
   - **OS**: Kali Linux
   - **Purpose**: Simulate attacks on the Active Directory environment

## Network Configuration
All VMs are networked to create an isolated environment that allows seamless communication and data flow between the machines. The network setup is as follows:
- **Network**: 192.168.10.0/24
- **Active Directory Server IP**: 192.168.10.7
- **Windows 10 Pro Client IP**: 192.168.10.100
- **Splunk Server IP**: 192.168.10.10
- **Kali Linux Attack Box IP**: 192.168.10.250
- ![image](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/636b5b82-fa62-4bed-abd7-973490092bd1)

## Installation and Setup
### Active Directory Server
1. Install Windows Server 2022.
2. Configure Active Directory Domain Services and DNS.
3. Create users: Raven Fury and John Doe.
4. Register the Windows 10 Pro client under the Raven Fury user.
5. 

### Windows 10 Pro Client
1. Install Windows 10 Pro.
2. Join the Active Directory domain.
3. Enable Remote Desktop Protocol (RDP).

### Splunk Server
1. Install Ubuntu Server 22.04.
2. Download and install Splunk Enterprise.
3. Configure Splunk to receive logs from the Active Directory Server and Windows 10 Pro client.
4. Install Splunk Universal Forwarder on both the Windows Server and Windows 10 Pro client.

### Kali Linux Attack Box
1. Install Kali Linux.
2. Configure the network settings to communicate with the Active Directory Server, Windows 10 Pro client, and Splunk Server.
3. Use Kali Linux tools to simulate various attack scenarios.

## Usage
1. **Monitor Security Events**: Use Splunk to monitor and analyze security events generated from the Active Directory and Windows 10 Pro client.
2. **Simulate Attacks**: Use Kali Linux to perform attacks on the Active Directory environment and observe the logs and alerts generated in Splunk.
3. **Incident Response**: Use the data collected in Splunk to practice incident response and forensic analysis.

## Attack Simulation
### RDP Attack
- Tool: Crowbar
- Target: Windows 10 Pro (Raven Fury user)
- Method: Using a custom password.txt list

**Screenshots**:
1. Alerts on the Splunk website
![Screenshot 2024-07-11 135438](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/1255c9ce-ab82-4887-8fc0-f156b86c3889)
2. RDP attack using Crowbar

![Screenshot 2024-07-11 134510](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/1f73913a-7f6a-46c0-be31-1b4e0e00e260)

3. Event 4625 (Failed login attempt) on Splunk
![Screenshot 2024-07-11 135501](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/2aed1fd5-1209-4bec-b16e-7ade911532ee)
4. Event 4624 (Successful login) on Splunk
![Screenshot 2024-07-11 135709](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/cbe8c4ff-5e14-4cf5-a170-46bda7f2c6e6)
5. Event 4524 details
![Screenshot 2024-07-11 135606](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/f8824b3c-2f69-45ed-a330-152e6e219454)
6. List of attacks by Crowbar
![Screenshot 2024-07-11 135733](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/d0558951-f4c1-4835-a970-1d9fd107ff4b)

### Testing Atomic Red Team
![Screenshot 2024-07-11 141527](https://github.com/Tanishq404E/SOC_Automation_Project/assets/70007965/f651bf38-2d71-436b-aa47-ed4bd0a3e458)

## Event Details
### Event 4624
- **Description**: An account was successfully logged on.
- **Importance**: Indicates a successful login, which can be used to track legitimate or unauthorized access.

### Event 4625
- **Description**: An account failed to log on.
- **Importance**: Indicates failed login attempts, which can signify brute-force attacks or other unauthorized access attempts.

## Future Enhancements
- Add more users and machines to the Active Directory environment.
- Integrate additional security tools for enhanced monitoring.
- Automate attack simulations and incident response workflows.

## Conclusion
This project provides a practical approach to learning about Active Directory, Splunk, and cybersecurity incident response. It offers a comprehensive setup for simulating and monitoring real-world scenarios, making it a valuable learning tool for anyone interested in cybersecurity.

## Contact
For any questions or feedback, feel free to contact me at:
- **Email**: tanishqtanwar1976@gmail.com
- **LinkedIn**: [LinkedIn Profile](https://www.linkedin.com/in/tanishq404e)
- **GitHub**: [GitHub Profile](https://github.com/tanishq404e)
