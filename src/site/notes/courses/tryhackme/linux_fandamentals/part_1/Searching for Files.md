---
{"dg-publish":true,"permalink":"/courses/tryhackme/linux-fandamentals/part-1/searching-for-files/","dgPassFrontmatter":true,"noteIcon":""}
---

Although it doesn't seem like it so far, one of the redeeming features of Linux is truly how efficient you can be with it. With that said, you can only be as efficient as you are familiar with it of course. As you interact with OSs such as Ubuntu over time, essential commands like those we've already covered will start to become muscle-memory.

One fantastic way to show just how efficient you can be with systems like this is using a set of commands to quickly search for files across the entire system that our user has access to. No need to consistently use `cd` and `ls` to find out what is where. Instead, we can use commands such as `find` to automate things like this for us!

This is where Linux starts to become a bit more intimidating to approach -- but we'll break this down and ease you into it.

## **Using Find**

The find command is fantastic in the sense that it can be used both very simply or rather complex depending upon what it is you want to do exactly. However, let's stick to the fundamentals first.

Take the snippet below; we can see a list of directories available to us:

![Pasted image 20230830162420.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162420.png)

1. Desktop
2. Documents
3. Pictures
4. folder1

Now, of course, directories can contain even more directories within themselves. It becomes a headache when we're having to look through every single one just to try and look for specific files. We can use `find` to do just this for us!

Let's start simple and assume that we already know the name of the file we're looking for — but can't remember where it is exactly! In this case, we're looking for "passwords.txt"

If we remember the filename, we can simply use `find -name passwords.txt` where the command will look through every folder in our current directory for that specific file like so:

![Pasted image 20230830162455.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162455.png)

"Find" has managed to _find_ the file — it turns out it is located in folder1/passwords.txt — sweet. But let's say that we don't know the name of the file, or want to search for every file that has an extension such as ".txt". Find let's us do that too!

We can simply use what's known as a wildcard (*) to search for anything that has .txt at the end. In our case, we want to find every .txt file that's in our current directory. We will construct a command such as `find -name *.txt` . Where "Find" has been able to _find_ every .txt file and has then given us the location of each one:

![Pasted image 20230830162532.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162532.png)

Find has managed to _find_:

1. "passwords.txt" located within "folder1"
2. "todo.txt" located within "Documents"

That wasn't so tough, huh!

  

## **Using Grep**

Another great utility that is a great one to learn about is the use of `grep`. The `grep` command allows us to search the contents of files for specific values that we are looking for.

Take for example, the access log of a web server. In this case, the access.log of a web server has 244 entries.

![Pasted image 20230830162604.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162604.png)

Using a command like `cat` isn't going to cut it too well here. Let's say for example if we wanted to search this log file to see the things that a certain user/IP address visited? Looking through 244 entries isn't all that efficient considering we want to find a specific value.

We can use `grep` to search the entire contents of this file for any entries of the value that we are searching for. Going with the example of a web server's access log, we want to see everything that the IP address "81.143.211.90" has visited (note that this is fictional)

![Pasted image 20230830162628.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830162628.png)

"Grep" has searched through this file and has shown us any entries of what we've provided and that is contained within this log file for the IP.

