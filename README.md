Install Cortex XDR Agent on Windows Endpoint (with Internet Connection)
Use the following workflow to install the Cortex XDR agent using the MSI file.
1.	Before installing the Cortex XDR agent on a Windows endpoint, verify that the system meets the requirements described in the Cortex XDR Agent for Windows Requirements.
2.	Download the Cortex XDR agent installer for Windows from Cortex XDR.
Ensure that you download the Windows installer for the Windows architecture (x64 or x86) installed on the endpoint.
3.	Run the MSI file on the endpoint.

The installer displays a welcome dialog.

 

4.	Click Next.
 

5.	Install the agent and next the installer will displays a User Account Control dialog.
 
6.	Click Yes.
7.	After you complete the installation, verify the Cortex XDR agent can establish a connection.


Install Cortex XDR Agent Windows Endpoint (without Internet Connection / Using VM Broker)
1.	Download the Cortex XDR agent installer for Windows from Cortex XDR.
2.	Open command prompt, run as administrator
3.	Execute command:
msiexec /i c:\install\cortexxdr.msi proxy_list=”IP_BROKER_VM:8888” 
Note: to install a Cortex XDR agent communicating through the Palo Alto Networks Broker VM , you must enter the Broker VM IP address and a port number. You can use default port 8888 or set another port number.

Sample
msiexec /i C:\XDR_Agent_for_Windows_x64.msi proxy_list=”192.168.1.100:8888”
Note: You are not permitted to configure port numbers between 0-1024 and 63000-65000, or port numbers 4369, 5671, 5672, 5986, 6379, 8000, 9100, 15672, 25672. Additionally, you are not permitted to reuse port numbers you already assigned to the Syslog Collector applet.
4.	After the initial installation, please verify the cortex agent are on endpoint list.


<img width="468" height="467" alt="image" src="https://github.com/user-attachments/assets/77f79931-c339-4837-ad56-0c6cd49e075e" />
