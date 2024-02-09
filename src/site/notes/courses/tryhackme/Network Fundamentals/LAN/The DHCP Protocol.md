---
{"dg-publish":true,"permalink":"/courses/tryhackme/network-fundamentals/lan/the-dhcp-protocol/","dgPassFrontmatter":true,"noteIcon":""}
---

P addresses can be assigned either manually, by entering them physically into a device, or automatically and most commonly by using a **DHCP** (**D**ynamic **H**ost **C**onfiguration **P**rotocol) server. When a device connects to a network, if it has not already been manually assigned an IP address, it sends out a request (DHCP Discover) to see if any DHCP servers are on the network. The DHCP server then replies back with an IP address the device could use (DHCP Offer). The device then sends a reply confirming it wants the offered IP Address (DHCP Request), and then lastly, the DHCP server sends a reply acknowledging this has been completed, and the device can start using the IP Address (DHCP ACK).

![Pasted image 20230912093726.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230912093726.png)  

Answer the questions below

What type of DHCP packet is used by a device to **retrieve an IP address?**

**Answer :** DHCP Discover

What type of DHCP packet does a device **send once it has been** **offered an IP address** by the DHCP server?

**Answer :** DHCP Request

Finally, **what is the last** DHCP packet that is sent to a device from a DHCP server?

**Answer :** DHCP ACK

