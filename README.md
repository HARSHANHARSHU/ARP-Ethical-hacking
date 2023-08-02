# ARP-Ethical-hacking
Step 1 − Install the VMware workstation and install the Kali Linux operating system.

Step 2 − Login into the Kali Linux using username pass “root, toor”.

Step 3 − Make sure you are connected to local LAN and check the IP address by typing the command ifconfig in the terminal

Step 4 − Open up the terminal and type “Ettercap –G” to start the graphical version of Ettercap

Step 5 − Now click the tab “sniff” in the menu bar and select “unified sniffing” and click OK to select the interface. We are going to use “eth0” which means Ethernet connection.

Step 6 − Now click the “hosts” tab in the menu bar and click “scan for hosts”. It will start scanning the whole network for the alive hosts.

Step 7 − Next, click the “hosts” tab and select “hosts list” to see the number of hosts available in the network. This list also includes the default gateway address. We have to be careful when we select the targets.

Step 8 − Now we have to choose the targets. In MITM, our target is the host machine, and the route will be the router address to forward the traffic. In an MITM attack, the attacker intercepts the network and sniffs the packets. So, we will add the victim as “target 1” and the router address as “target 2.”

In VMware environment, the default gateway will always end with “2” because “1” is assigned to the physical machine.

Step 9 − In this scenario, our target is “192.168.121.129” and the router is “192.168.121.2”. So we will add target 1 as victim IP and target 2 as router IP.

Step 10 − Now click on “MITM” and click “ARP poisoning”. Thereafter, check the option “Sniff remote connections” and click OK

Step 11 − Click “start” and select “start sniffing”. This will start ARP poisoning in the network which means we have enabled our network card in “promiscuous mode” and now the local traffic can be sniffed.

Note − We have allowed only HTTP sniffing with Ettercap, so don’t expect HTTPS packets to be sniffed with this process.

Step 12 − Now it’s time to see the results; if our victim logged into some websites. You can see the results in the toolbar of Ettercap.
