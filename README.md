# Azure-Compute-and-Networking
This Azure Compute and Networking Project shows the examination of network traffic analysis between two Azure Virtual Machines using Wireshark and experiment with Network Security Groups
 <section id="header-section">
  <h1>Environments and Technologies Used</h1>
  <ul>
    <li>Microsoft Azure (Virtual Machines/Compute)</li>
    <li>Remote Desktop</li>
    <li>Various Command-Line Tools</li>
    <li>Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)</li>
    <li>Wireshark (Protocol Analyzer)</li>
  </ul>
  <h1>Operating Systems Used</h1>
  <ul>
    <li>Windows 10 (21H2)</li>
    <li>Ubuntu Server 20.04</li>
  </ul>
 </section>
 <section id="steps">
  <h1>Actions and Observations</h1>
  <h3>Creating The Resources</h3>
    <p>I created a Resource Group in Microsoft Azure. Moreover, I set up a Windows 10 Virtual Machine and a Linux (Ubuntu) Virtual Machine. While configuring the Windows 10 VM, I allowed it to create a Virtual Network (Vnet) and Subnet. Lastly, I observed the Virtual Machine within the network using Network Watcher.</p>
    <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/c8d77a6f-83e2-4a7d-bdbb-0208f9a58a1d">  
  <h3>Observe ICMP Traffic</h3>
   <p>After creating the Virtual Machines, I used Remote Desktop to connect to the Windows 10 VM. I installed Wireshark and filtered for ICMP traffic. By pinging the private IP address of the Ubuntu VM within the Windows 10 VM, I observed ping requests and replies in Wireshark. Then, I pinged www.google.com and examined the traffic.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/a3c2ac1d-2419-4c30-a987-8fa589881aa4">
   <p>I initiated a perpetual ping between the Windows 10 and Ubuntu VMs. Disrupting the inbound ICMP traffic in Azure, I observed the interruption in communication between the VMs. Finally, I stopped the ping at the end of this experiment.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/b735ec2f-0928-46d3-b922-3121d3eb1270">  
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/0b68b707-11dd-4043-8e22-366c6ffbdad8">
  <h3>Observe SSH Traffic</h3>
   <p>Next, I securely accessed the Ubuntu VM via SSH, enabling me to closely monitor SSH traffic between the Windows 10 VM and the Ubuntu VM. Furthermore, I executed various Linux commands to observe the resulting SSH traffic spikes in WireShark.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/2f9e0d87-c012-4c65-9b7a-3cec03f211b5">
 <h3>Observe DHCP Traffic</h3>
   <p>Next, I monitored DHCP traffic and made an attempt to assign a new IP address. I closely observed the DHCP traffic within WireShark to analyze the results.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/26979cfd-fdc8-4ace-8131-53ad7510eacb"> 
 <h3>Observe DNS Traffic</h3>
   <p>Next, I filtered for DNS traffic and used the nslookup command in PowerShell to examine DNS queries. I specifically observed the IP addresses associated with Google. This allowed me to closely observe the DNS traffic displayed in WireShark.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/c4a4cdd9-2504-48a7-b7b7-45584ab0f290">
 <h3>Observe RDP Traffic</h3>
   <p>In WireShark, I applied a filter for RDP traffic only (tcp.port == 3389) to witness the constant live streaming of the RDP protocol between two computers.</p>
   <img width="900" height="500" alt="image" src="https://github.com/SamEshaia/Azure-Compute-and-Networking/assets/124312452/f5a72a34-6a7a-4ef0-a3ee-2eaaec02a5c7">
</section>
