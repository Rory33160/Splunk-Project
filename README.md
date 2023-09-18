# Splunk-Project
Splunk Lab ingesting data into SEIM (Splunk Forwarder)
 

<h2>Description</h2>
Project consist of installing Splunk and Splunk Forwarder. Using Splunk Forwarder to ingest data from home network for and monitor traffic.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Splunk</b> 
- <b>Splunk Forwarder</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (21H2)

<h2>Program walk-through:</h2>
Download and install Splunk and Splunk Forwarder for the purpose of monitoring local network traffic.


![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/054b6111-c12b-4d41-940f-2faf5a70a2c2)


Select the OS, for me - I am choosing  Windows 64 bit because I am using Windows 10

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/b9451835-357d-4cd4-a46b-866e2dc3c7fd)

Saving Splunk 9.1.0.1 to my computer


![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/5270d102-f1b9-4b74-9307-7e5e0335f454)

Create a username and password, for demontration purposes I am using Admin and sign in to make sure it works.

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/e9b69d37-f29d-4c21-ac39-e09d5bcc5026)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/c3608e5f-14e2-4eae-a97a-c084fba922ea)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/156e4d35-05ba-4912-9cf7-161a9b44d4fb)

Download Splunk Universal Forwarder for Windows 64-bit

Accept the user agreement of course.

Where it says:  “Use this Universal Forwarder with:…………

Select > On premises Splunk Cloud instance then select next

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/8bbe3f25-ecaf-4a44-987e-03570849050c)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/1b656687-fd25-445f-9bff-ae543f965850)

Setting up Universal Forwarder. 

The configuration screen ask for the local IP address and port.

Ipconfig will provide the IP address and I am using port 9997 or the default port suggested

Enter ip and port .

Click next then finish.


![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/e9d4c942-844f-4a99-8a1d-af2578dd57f9)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/b9e886bb-680f-4c0c-af7f-910092f9d895)


Go back to Splunk to set up  Universal Forwarder

Select the pull down menu at the top right corner  and click “Add Data”

Error message:

 “No Clients or apps are currently available on this deployment server“



![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/10b9af13-6acf-4391-8d21-38d0f791e146)


![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/17011192-a423-4ee8-a5e8-6c9e397e5cbc)

A Little troubleshooting can not fix. 
The immediate suspect is port access
Fire up Powershell and tested the connection ports for Splunk and Splunk Universal Forwarder.

Powershell command Splunk:
Test-connection  -computername your IP address here port 8000
The result for TCPTestSucceesed: True

Powershell command Splunk Forwarder:
Test-connection  -computername your IP address here port 9997
The result for TCPTestSucceesed: False


We can see that Splunk Forwarder is not connecting to port 9997



![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/ba65eb87-d48b-4b41-a3ff-26c6657a4d23)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/8e674db9-743a-4ac9-a408-f34935458613)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/c6b5d1a8-fcb0-40dc-88c2-a4f3500c8ea4)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/51ee45b8-96d1-4d09-802e-d510f437a834)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/8371cad9-0eb6-41d5-9cae-ab5c26ce7f9d)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/492227bb-7874-4a43-a380-eb5d6c58c959)

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/e8482e1f-17f9-45c5-8299-c17991910a36) 

![image](https://github.com/Rory33160/Splunk-Project/assets/47018034/2dd4db03-3bfd-4e59-8533-056c78a114a3)


