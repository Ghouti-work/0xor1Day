---
{"dg-publish":true,"permalink":"/courses/hack-the-box/kioptrix-level-1/","dgPassFrontmatter":true,"noteIcon":""}
---



<iframe width="560" height="315" src="https://www.youtube.com/embed/zO6NdOjgwY0?si=w5ueL8Z4U7p7YmnL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
---
#### find the ip
if we need to know the ip of our machine than we need to use : `ip confige` 
after that we need to know the target ip , than we use the : `netdiscover `
	or `netdicover -r our-ip(xxx.xxx.xxx.xxx)`
- ![Pasted image 20230927030943.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927030943.png)
- the **IP** is 192.168.232.132
#### scan network
than we need to scan  the ip we use [[nmap\|nmap]] for this operation and all this parameter are in the documentation .
- TCP scan
- ![Pasted image 20230927030729.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927030729.png)
-  UDP scan 
- ![Pasted image 20230927031237.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927031237.png)
- ###### TCP scan result 
- ssh open port 22, tcp open port 80(http),111(rgcbind) ... to the end  .
- ![Pasted image 20230927031606.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927031606.png)
-  ![Pasted image 20230927031842.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927031842.png)
- ![Pasted image 20230927031935.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927031935.png)

#### look at HTTP 
![Pasted image 20230927032250.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927032250.png)
- just tip the IP the browser .
- ![Pasted image 20230927032542.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927032542.png)

#### find the host using nikto 
![Screenshot from 2023-09-27 03-26-22.png](/img/user/courses/HackTheBox/img/Screenshot%20from%202023-09-27%2003-26-22.png)

![Pasted image 20230927032653.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927032653.png)
service
![Pasted image 20230927033019.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927033019.png)
version 
![Pasted image 20230927033214.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927033214.png)
or using curl
![Pasted image 20230927033333.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927033333.png)

---

![Pasted image 20230927033533.png](/img/user/courses/HackTheBox/img/Pasted%20image%2020230927033533.png)

use word list fron ==user/shar/wordlist/dirbbuster_lis/...== 
