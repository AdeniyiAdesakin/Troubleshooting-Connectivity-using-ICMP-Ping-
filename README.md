<h1>Troubleshooting Connectivity with ICMP (Ping)</h1>
<br>
<h3>Faced an initial challenge joining the client VMs(Windows 10 & 11) to ADDS, I had to enable Internet Control Message Protocol(Ping) using a command line via Command Prompt. This process facilitated network discovery and communication</h3>
<br>

<p>1. I tried to ping one of the computer but couldn’t. Packets: Sent = 4, Received = 0, Lost =4 (100% Loss). In short, the computer couldn’t find each other.</p>
<p align="center"><img src="https://i.imgur.com/tsQedXI.png" height="50%" width="50%"/>

<p>2. To solve this issue and allow ICMP, I used the following cmd prompt; <I>"netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=allow"</I>, And this issue was resolved.</p>
<p align="center"><img src="https://i.imgur.com/mMfAGXX.png" height="50%" width="50%"/>
