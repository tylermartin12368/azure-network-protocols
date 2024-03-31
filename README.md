<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Create Azure Virtual Machines. Make one virtual machine operate on Windows and the other on Linux.
- Step 2: Use Remote Desktop to remote into the Azure Virtual Machine operating on Windows.
- Step 3: Download Wireshark onto the Azure Virtual Machine. It will be used as our network analyzer.
- Step 4: Use Wireshark and Windows Powershell to test different protocals to observe what traffic occurs.

<h2>Actions and Observations</h2>

![Screenshot (1)](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/10c93696-e899-4565-ba16-5792bb2b718a)
</p>
<p>
The first step we are going to do is create our Azure Virtual Machines. In order to do this we will need to create a resource group before creating the virtual machines. We create our virtual machines into our newly created resource group, so that we can manage these resources in one area. When creating the Azure Virtual machines, we will need to make sure that they are on diffrent operating systems (Windows and Linux) and are on the same virtual network. If they are not on the same virtual network, then when using the ssh protocal (later in the lab) you won't be able to communicate with your other virtual machine. 
</p>
<br />

![Screenshot (2)](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/2ace5ab2-14bc-4945-adc5-5c71edf13f4f)
</p>
<p>
Once our Azure Virtual Machines are up and running, then we can use remote desktop and remote into the virtual machine that is operating on Windows. Once remoted into the virtual machine, then we will need to download Wireshark. Wireshark will allow us to observe different kinds of traffic when using different protocals. We will use Windows Powershell to enter commands to generate traffice between both virtual machines. We can use Wireshark to observe all sorts of traffic like ICMP. We use this protocol in order to make sure that data the we are sending is getting to its destination. We can create an Inbound Security Rule on the virtual machine operating on Linux, to deny all ICMP traffic. When this rule is created you will start to notice that you will get a "no response found" error. That is a result of data not being able to arrive at its destination anymore due to this rule being created.   
</p>
<br />

![20240318_221406](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/faaed625-b8d7-4489-811f-c4aa3ed97408)
</p>
<p>
DNS traffic is also something that we can observe. DNS is used to convert domain names into IP addresses that you can then use to browse through that domain. An example of a domain would be netflix.com. We enter the domain in our browser which will pull the IP address of that domain and then it will send a response back to our IP address. This is what allows us to browse through websites. We can see this take action in Wireshark when we use nslookup on specific domains through Windows Powershell. Information is being sent to the IP address of the domain we are trying to interact with and is sending information back to our IP address.  
</p>
<br />
