---
{"dg-publish":true,"permalink":"/courses/tryhackme/linux-fandamentals/part-1/interacting-with-the-filesystem/","dgPassFrontmatter":true,"noteIcon":""}
---

So far we've only covered the "**echo**" and "**whoami**" commands. Not all that useful when you consider things that we need to do - including navigating the filesystem, read and write to it as well.

In this task, we're going to be learning the commands so that we can do just that. Just like the previous task, I'll display the commands in the table in the next heading & show examples of these commands being used.

  

## Interacting With the Filesystem

As I previously stated, being able to navigate the machine that you are logged into without relying on a desktop environment is pretty important. After all, what's the point of logging in if we can't go anywhere?

|   |   |
|---|---|
|Command|Full Name|
|ls|listing|
|cd|change directory|
|cat|concatenate|
|pwd|print working directory|

  

### Listing Files in Our Current Directory (ls)

Before we can do anything such as finding out the contents of any files or folders, we need to know what exists in the first place. This can be done using the "ls" command (short for listing)
![Pasted image 20230830161754.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830161754.png)

In the screenshot above, we can see there are the following directories/folders:

- Important Files
- My Documents
- Notes
- Pictures

Great! You can probably take a guess as to what to expect a folder to contain given by its name.

_Pro tip: You can list the contents of a directory without having to navigate to it by using **ls** and the name of the directory. I.e. `ls Pictures`_

###   

### Changing Our Current Directory (cd)

Now that we know what folders exist, we need to use the "**cd**" command (short for **c**hange **d**irectory) to change to that directory. Say if I wanted to open the "Pictures" directory - I'd do "**cd Pictures**". Where again, we want to find out the contents of this "Pictures" directory and to do so, we'd use "**ls**" again:
![Pasted image 20230830161850.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830161850.png)

In this case, it looks like there are 4 pictures of dogs!

  

### Outputting the Contents of a File (cat)

Whilst knowing about the existence of files is great — it's not all that useful unless we're able to view the contents of them.

We will come on to discuss some of the tools available to us that allows us to transfer files from one machine to another in a later room. But for now, we're going to talk about simply seeing the contents of text files using a command called "**cat".**

"Cat" is short for concatenating & is a fantastic way us to output the contents of files (not just text files!).

In the screenshot below, you can see how I have combined the use of "ls" to list the files within a directory called "Documents":

![Pasted image 20230830161920.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830161920.png)

We've applied some knowledge from earlier in this task to do the following:

1. Used "**ls**" to let us know what files are available in the "Documents" folder of this machine. In this case, it is called "todo.txt".
2. We have then used `cat todo.txt` to concatenate/output the contents of this "todo.txt" file, where the contents are "Here's something important for me to do later!"

_Pro tip: You can use `cat` to output the contents of a file within directories without having to navigate to it by using **cat** and the name of the directory. I.e. `cat /home/ubuntu/Documents/todo.txt`_

Sometimes things like usernames, passwords (yes - really...), flags or configuration settings are stored within files where "cat" can be used to retrieve these.

  

### Finding out the full Path to our Current Working Directory (pwd)

You'll notice as you progress through navigating your Linux machine, the name of the directory that you are currently working in will be listed in your terminal.

It's easy to lose track of where we are on the filesystem exactly, which is why I want to introduce "**pwd**". This stands for **p**rint **w**orking **d**irectory.

Using the example machine from before, we are currently in the "Documents" folder — but where is this exactly on the Linux machine's filesystem? We can find this out using this "pwd" command like within the screenshot below:
![Pasted image 20230830162001.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162001.png)

**Let's break this down:

1. We already know we're in "Documents" thanks to our terminal, but at this point in time, we have no idea where "Documents" is stored so that we can get back to it easily in the future.
2. I have used the "**pwd**" (**p**rint **w**orking **d**irectory) command to find the full file path of this "Documents" folder.
3. We're helpfully told by Linux that this "Documents" directory is stored at "/home/ubuntu/Documents" on the machine — great to know!
4. Now in the future, if we find ourselves in a different location, we can just use `cd /home/ubuntu/Documents` to change our working directory to this "Documents" directory