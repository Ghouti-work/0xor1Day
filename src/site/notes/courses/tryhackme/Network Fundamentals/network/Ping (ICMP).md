---
{"dg-publish":true,"permalink":"/courses/tryhackme/network-fundamentals/network/ping-icmp/","dgPassFrontmatter":true,"noteIcon":""}
---


Ping is one of the most fundamental network tools available to us. Ping uses **ICMP** (**I**nternet **C**ontrol **M**essage **P**rotocol) packets to determine the performance of a connection between devices, for example, if the connection exists or is reliable.

  

The time taken for ICMP packets travelling between devices is measured by ping, such as in the screenshot below. This measuring is done using ICMP's echo packet and then ICMP's echo reply from the target device.

  

Pings can be performed against devices on a network, such as your home network or resources like websites. This tool can be easily used and comes installed on Operating Systems (OSs) such as Linux and Windows. The syntax to do a simple ping is 
```shell
ping IP address or website URL 
```
. Let's see this in action in the screenshot below.

  

![Pasted image 20230902101654.png](/img/user/courses/tryhackme/Network%20Fundamentals/img/Pasted%20image%2020230902101654.png)

  

Here we are pinging a device that has the private address of _192.168.1.254_. Ping informs us that we have sent six ICMP packets, all of which were received with an average time of 4.16 seconds.

  

Now you are going to do the same thing to ping the address of "**8.8.8.8**" on the deployable website in this task. Pinging the correct address will reveal a flag to answer the following question below.

Answer the questions below

What protocol does ping use?

**ANSWER**: ICMP

What is the syntax to ping 10.10.10.10?  

**ANSWER**: ping 10.10.10.10

What flag do you get when you ping 8.8.8.8?

**ANSWER**: THM{I_PINGED_THE_SERVER}