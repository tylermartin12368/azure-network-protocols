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
- Step 4: Use Wireshark and Windows Power Shell to test different protocals to observe what traffic occurs.

<h2>Actions and Observations</h2>

![Screenshot (1)](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/10c93696-e899-4565-ba16-5792bb2b718a)
</p>
<p>
The first step we are going to do is create our Azure Virtual Machines. In order to do this we will need to create a resource group before creating the virtual machines. We create our virtual machines into our newly created resource group, so that we can manage these resources in one area. When creating the Azure Virtual machines, we will need to make sure that they are on diffrent operating systems (Windows and Linux) and are on the same virtual network. If they are not on the same virtual network, then when using the ssh protocal you will not be able to communicate with your other virtual machine. 
</p>
<br />

![Screenshot (2)](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/2ace5ab2-14bc-4945-adc5-5c71edf13f4f)
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![20240318_221406](https://github.com/tylermartin12368/azure-network-protocols/assets/161632103/faaed625-b8d7-4489-811f-c4aa3ed97408)
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
