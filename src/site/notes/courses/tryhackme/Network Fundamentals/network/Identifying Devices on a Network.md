---
{"dg-publish":true,"permalink":"/courses/tryhackme/network-fundamentals/network/identifying-devices-on-a-network/","dgPassFrontmatter":true,"noteIcon":""}
---


To communicate and maintain order, devices must be both identifying and identifiable on a network. What use is it if you don't know whom you're talking to at the end of the day?

Devices on a network are very similar to humans in the fact that we have two ways of being identified:

- Our Name
- Our Fingerprints

Now we can change our name through deed poll, but we can't, however, change our fingerprints. Every human has an individual set of fingerprints which means that even if they change their name, there is still an identity behind it. Devices have the same thing: two means of identification, with one being permeable. These are:

- An IP Address
- A Media Access Control (MAC) Address -- think of this as being similar to a serial number.

### 

### **IP Addresses**

Briefly, an IP address (or **I**nternet **P**rotocol) address can be used as a way of identifying a host on a network for a period of time, where that IP address can then be associated with another device without the IP address changing. First, let's split up precisely what an IP address is in the diagram below:

![Pasted image 20230901014506.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230901014506.png)


An **IP** address is a set of numbers that are divided into four octets. The value of each octet will summarise to be the IP address of the device on the network. This number is calculated through a technique known as IP addressing & subnetting, but that is for another day. What's important to understand here is that IP addresses can change from device to device but cannot be active simultaneously more than once within the same network.

IP Addresses follow a set of standards known as protocols. These protocols are the backbone of networking and force many devices to communicate in the same language, which is something that we'll come onto another time. However, we should recall that devices can be on both a private and public network. Depending on where they are will determine what type of IP address they have: a public or private IP address.

A public address is used to identify the device on the Internet, whereas a private address is used to identify a device amongst other devices. Take the table & screenshot below as an example. Here we have two devices on a private network:

  

|   |   |   |
|---|---|---|
|**Device Name**|**IP Address**|**IP Address Type**|
|DESKTOP-KJE57FD|192.168.1.77|Private|
|DESKTOP-KJE57FD|86.157.52.21|Public|
|CMNatic-PC|192.168.1.74|Private|
|CMNatic-PC|86.157.52.21|Public|

  
![Pasted image 20230901014528.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230901014528.png)

These two devices will be able to use their private IP addresses to communicate with each other. However, any data sent to the Internet from either of these devices will be identified by the same public IP address. Public IP addresses are given by your **I**nternet **S**ervice **P**rovider (or **ISP**) at a monthly fee (your bill!)

![Pasted image 20230901014619.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230901014619.png)

As more and more devices become connected, it is becoming increasingly harder to get a public address that isn't already in use. For example, Cisco, an industry giant in the world of networking, estimated that there would be approximately 50 billion devices connected on the Internet by the end of 2021. [(Cisco., 2021)](https://www.cisco.com/c/dam/en_us/about/ac79/docs/innov/IoT_IBSG_0411FINAL.pdf). Enter IP address versions. So far, we have only discussed one version of the Internet Protocol addressing scheme known as IPv4, which uses a numbering system of 2^32 IP addresses (4.29 billion) -- so you can see why there is such a shortage!

IPv6 is a new iteration of the Internet Protocol addressing scheme to help tackle this issue. Although it is seemingly more daunting, it boasts a few benefits:

- Supports up to 2^128 of IP addresses (340 trillion-plus), resolving the issues faced with IPv4
- More efficient due to new methodologies

The screenshot below compares both an IPv6 and IPv4 address.

![Pasted image 20230901014733.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230901014733.png)  

**MAC Addresses  
**

Devices on a network will all have a physical network interface, which is a microchip board found on the device's motherboard. This network interface is assigned a unique address at the factory it was built at, called a **MAC** (**M**edia **A**ccess **C**ontrol ) address. The MAC address is a **twelve-character** hexadecimal number (_a base sixteen numbering system used in computing to represent numbers_) split into two's and separated by a colon. These colons are considered separators. For example, _a4:c3:f0:85:ac:2d_. The first six characters represent the company that made the network interface, and the last six is a unique number.

  ![Pasted image 20230901014757.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230901014757.png)

  

However, an interesting thing with MAC addresses is that they can be faked or "spoofed" in a process known as spoofing. This spoofing occurs when a networked device pretends to identify as another using its MAC address. When this occurs, it can often break poorly implemented security designs that assume that devices talking on a network are trustworthy. Take the following scenario: A firewall is configured to allow any communication going to and from the MAC address of the administrator. If a device were to pretend or "spoof" this MAC address, the firewall would now think that it is receiving communication from the administrator when it isn't.

Places such as cafes, coffee shops, and hotels alike often use MAC address control when using their "Guest "or "Public" Wi-Fi. This configuration could offer better services, i.e. a faster connection for a price if you are willing to pay the fee per device.  The **interactive lab attached to this task** has been made to replicate this scenario!

**Practical**  

The interactive labs simulate a hotel Wi-Fi network where you have to pay for the service. You'll note that the router is not allowing Bob's packets ( blue) to the TryHackMe website and is placing them in the bin, but Alice's packets (green) are going through fine because she has paid for Wi-Fi. Try changing Bob's MAC address to the same as Alice's to see what happens.  

Deploy the interactive lab and proceed to answer the following questions below.

Answer the questions below

What does the term "IP" stand for?

answer: Internet Protocol

What is each section of an IP address called?  

answer: octet

How many sections (in digits) does an IP address have?   

answer: 4

What does the term "MAC" stand for?  

answer: **M**edia **A**ccess **C**ontrol )

Deploy the interactive lab using the "View Site" button and spoof your MAC address to access the site.  What is the flag?

