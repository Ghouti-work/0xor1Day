---
{"dg-publish":true,"permalink":"/courses/tryhackme/linux-fandamentals/part-3/general-useful-utilities/","dgPassFrontmatter":true,"noteIcon":""}
---

**Downloading Files**

A pretty fundamental feature of computing is the ability to transfer files. For example, you may want to download a program, a script, or even a picture. Thankfully for us, there are multiple ways in which we can retrieve these files.

 We're going to cover the use of `wget` .  This command allows us to download files from the web via HTTP -- as if you were accessing the file in your browser. We simply need to provide the address of the resource that we wish to download. For example, if I wanted to download a file named "myfile.txt" onto my machine, assuming I knew the web address it -- it would look something like this:
 
```terminal
`wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt`
```
  

**Transferring Files From Your Host - SCP (SSH)**

Secure copy, or SCP, is just that -- a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using the SSH protocol to provide both authentication and encryption.

Working on a model of SOURCE and DESTINATION, SCP allows you to:

- Copy files & directories from your current system to a remote system
- Copy files & directories from a remote system to your current system

Provided that we know usernames and passwords for a user on your current system and a user on the remote system. For example, let's copy an example file from our machine to a remote machine, which I have neatly laid out in the table below:

|   |   |
|---|---|
|Variable|Value|
|The IP address of the remote system|192.168.1.30|
|User on the remote system|ubuntu|
|Name of the file on the local system|important.txt|
|Name that we wish to store the file as on the remote system|transferred.txt|

With this information, let's craft our `scp` command (remembering that the format of SCP is just SOURCE and DESTINATION)

`scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt`

And now let's reverse this and layout the syntax for using `scp` to copy a file from a remote computer that we're not logged into 

|   |   |
|---|---|
|Variable|Value|
|IP address of the remote system|192.168.1.30|
|User on the remote system|ubuntu|
|Name of the file on the remote system|documents.txt|
|Name that we wish to store the file as on our system|notes.txt|

The command will now look like the following: `scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt` 

**Serving Files From Your Host - WEB**

Ubuntu machines come pre-packaged with python3. Python helpfully provides a lightweight and easy-to-use module called "HTTPServer". This module turns your computer into a quick and easy web server that you can use to serve your own files, where they can then be downloaded by another computing using commands such as `curl` and `wget`. 

Python3's "HTTPServer" will serve the files in the directory that you run the command, but this can be changed by providing options that can be found in the manual pages. Simply, all we need to do is run `python3 -m  http.server` to start the module! In the screenshot below, we are serving from a directory called "webserver", which has a single named "file".

![Pasted image 20230831125548.png](/img/user/courses/tryhackme/linux_fandamentals/part_3/img/Pasted%20image%2020230831125548.png)
  

Now, let's use `wget` to download the file using the computer's IP address and the name of the file. One flaw with this module is that you have no way of indexing, so you must know the exact name and location of the file that you wish to use. This is why I prefer to use Updog. [What's Updog](https://github.com/sc0tfree/updog)? A more advanced yet lightweight webserver. But for now, let's stick to using Python's "HTTP Server".

![Pasted image 20230831125622.png](/img/user/courses/tryhackme/linux_fandamentals/part_3/img/Pasted%20image%2020230831125622.png)

In the screenshot above, we can see that `wget` has successfully downloaded the file named "file" to our machine. This request is logged by SimpleHTTPServer much as any web server would, which I have captured in the screenshot below.

![Pasted image 20230831125642.png](/img/user/courses/tryhackme/linux_fandamentals/part_3/img/Pasted%20image%2020230831125642.png)
