# Deploying-Log-Analytics-Agent

# Goal is to connect Azure VM to Log Analytics Workspace
- Why? Microsoft Defender can better protect your resources if it knows what's going on within your resources. 
- Log Analytics Workspace is within Microsoft Defender and Defender uses that data collected.


# Create a Log Anaytics Workspace
- Go to Microsoft Defender for Cloud and enable auto provisioning for log analtics agent for Azure VMs.
- Connect the azure vm to the LAW that you created
- Now the LAW agent will be installed on the vm and collect data. 
- Then Microsoft Defender will take the data and look for threats based on data collected.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176020740-548e653b-3673-4b95-b20b-75b96e918cbc.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>



# Use Cases: Create LAW and connect a VM to the LAW for Microsoft Defender to evaluate
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176021100-4f3c52e9-9c3b-4cfe-b6b8-4364cbfce4d7.png" height="45%" width="45%" alt="Azure LAW"/>

<p/>


# Enable auto-provisioning for Azure Virtual Machines and connect the LAW 
- Microsoft Defender for Cloud > Environment Settings > Auto provisioning > enable Log analytics agent for Azure VMs 
- Connect the LAW that you want Azure VMs to link to
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176021660-d295d79d-8cf4-44eb-a998-33c4cb55ad96.png" height="155%" width="155%" alt="Azure LAW"/>

<p/>


# How to enable the collection of the different security-based events?
- At the OS level, admins can view security events on Event Viewer - where it shows the different types of events from Windows Logs
- It will tell you the event ID and the general details of the event itself.
- When someone tries to log in, an event is generated at the OS level in the event viewer within the security windows log.
- For Microsoft Defender for Cloud to view these events at the OS level for each virtual machine, it must be given the ability to collect the events.

# How to direct all of the events collected to the LAW for MIcrosoft Defender for Cloud to look for threats?
- Microsoft Defender for Cloud > Select LAW workspace created > Defender Plans > Enable Microsoft Defender for Cloud plans and is turned on for Servers and SQL servers
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176024642-cf5b01bd-df9c-4c2c-a695-57a111a77756.png" height="156%" width="155%" alt="Azure LAW"/>

<p/>

# Enable data collection by selecting "Common"
- Now the virtual machines that are in your environment will send their data to the LAW 
- Plus, Microsoft Defender will be able to collect those events and detect threats
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176025133-5973bd63-7cc4-4a3b-b9f1-6b31e5de6314.png" height="156%" width="155%" alt="Azure LAW"/>

<p/>


# What is the Inventory section for Microsoft Defender for Cloud?
- Inventory - gives you a view of the security posture of the resources that are being monitored.
- You can view the recommendations from a resource point of view
- You can also view alerts and installed applications from a resource perspective
- Whereas on the overview, you get a list of all the recommendations for the Subscription


# Microsoft Defender for Cloud - Workload Protection (Enhaced Security features under the Enhanced Plan)
- File Integrity Monitoring -examines OS files, application software, Linux system files
- Change tracking - log analytics agent sends data reporting the state of items on the machine
- Files - can mention which files and folders to monitor
- Cloud - can connect machines your AWS cloud environment
- Applications - can create an whitelist applications
- Identify - help identify any sort of potential malware, outdates or unauthorized applications
- Groups - applications can be segregated into groups if they run similar types of applications
- Rules - can define rules to configure how applications are managed


# More features for workload protection
- Network Security Groups - helps to harden the NSG rules
- Identification - uses an internal machine learning algorithm to provide indicators on how to harden the NSG
- Alerts - can get alerts if traffic flowing via the resource if not within the defined IP range




