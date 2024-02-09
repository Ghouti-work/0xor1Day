---
{"dg-publish":true,"permalink":"/courses/tryhackme/getting-started-with-open-vpn/","dgPassFrontmatter":true,"noteIcon":""}
---

# **How do I get started?**

We have a **[room dedicated to helping](https://tryhackme.com/room/openvpn)** you install the lightweight software needed to connect you to our network. The room visualizes the installation process for the operating system of your choice! We also have a [Windows](https://intercom.help/tryhackme_help/en/articles/6496034-connecting-to-openvpn-on-windows) and [Linux](https://intercom.help/tryhackme_help/en/articles/6496038-connecting-to-openvpn-on-linux) guide to help you connect to our network.

## The "Access" page:

[![The Access Page](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666243/73ccde832ca5932c4ec0844c/CYWJmzj.png)](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666243/73ccde832ca5932c4ec0844c/CYWJmzj.png)

The access page is the reference point for anything TryHackMe VPN related.  
Hopefully, you will only have to visit this once to download your TryHackMe configuration file for OpenVPN! However, it is one of the first ports of call in managing your TryHackMe VPN and troubleshooting.

# **Choosing a VPN server:**

TryHackMe has multiple VPN servers placed throughout various geographic regions to help keep your ping low and the connection stable. At the time of writing, TryHackMe has the following:

|   |   |
|---|---|
|Server Name|Region|
|EU-Regular-1|Europe|
|EU-Regular-2|Europe|
|EU-Regular-3|Europe|
|EU-VIP-1|Europe|
|EU-VIP-2|Europe|
|US-West-Regular-1|United States - West Coast|
|US-East-Regular-1|United States - East Coast|
|US-West-VIP-1|United States - West Coast|
|IN-Regular-1|India|
|AU-Regular-1|Australia|

At times there may be many concurrent users on the site, which is why some regions, such as EU, have two regular servers for load balancing.

# **Verifying connectivity:**

Upon successful connection, OpenVPN will produce a message such as the one below:

**DAY MONTH DATE HH:MM: SS YYYY Initialization Sequence Completed**

If you have any doubts as to whether or not you are connected, deploy the instance attached to **[[Task 6] Check you're connected](https://tryhackme.com/room/openvpn)** in the OpenVPN room. After a few minutes, you can visit the IP address of the instance assigned to you in your browser.

[![Deploy OpenVPN room](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666247/9b9b3588f01bd1ac9b0a1073/QI2JRXh.png)](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666247/9b9b3588f01bd1ac9b0a1073/QI2JRXh.png)

The IP address you need to visit will differ from that in the screenshot above.

You should see the following in the browser of the device that you are connecting from. If so, you are connected!

[![Confirming Connectivity](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666253/5ff69614c9d88aca8cf25f6c/Zd2f7jK.png)](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666253/5ff69614c9d88aca8cf25f6c/Zd2f7jK.png)

# **OpenVPN errors & troubleshooting:**

When configuration files are generated with formatting issues, OpenVPN will fail with an error similar to the following if yours has been generated with errors:

**Mon Jun 15 22:28:35 2020 Cannot load inline certificate file**

**Mon Jun 15 22:28:35 2020 Exiting due to fatal error**

To fix this, switch VPN servers and press "Regenerate". For example, suppose you were on EU-Regular-1. In that case, you should swap to **EU-Regular-2** and press "Regenerate" like below:

[![Regenerating OpenVPN onfiguration File](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666259/ae109529e8864c5a8427d489/uQ8L7jX.png)](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666259/ae109529e8864c5a8427d489/uQ8L7jX.png)

Please wait at least 2 minutes before pressing "Download My Configuration File." This will allow enough time for a new configuration file to be generated for you. After downloading, we suggest renaming and appending a `2` to the end to ensure you connect with this file in the future. Check out the [troubleshooting](https://intercom.help/tryhackme_help/en/articles/6496029-openvpn-general-troubleshooting-detailed) page for more guidance if you have issues that do not relate to your config file.

[![Renaming new Configuration File](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666266/82fc282d33cb33ba599dc5be/ENFOZLh.png)](https://tryhackme-ad00cffb3f37.intercom-attachments-1.com/i/o/591666266/82fc282d33cb33ba599dc5be/ENFOZLh.png)