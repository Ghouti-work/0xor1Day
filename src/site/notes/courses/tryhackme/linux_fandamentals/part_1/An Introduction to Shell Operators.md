---
{"dg-publish":true,"permalink":"/courses/tryhackme/linux-fandamentals/part-1/an-introduction-to-shell-operators/","dgPassFrontmatter":true,"noteIcon":""}
---

Linux operators are a fantastic way to power up your knowledge of working with Linux. There are a few important operators that are worth noting. We'll cover the basics and break them down accordingly to bite-sized chunks.

At an overview, I'm going to be showcasing the following operators:

|   |   |
|---|---|
|Symbol / Operator|Description|
|&|This operator allows you to run commands in the background of your terminal.|
|&&|This operator allows you to combine multiple commands together in one line of your terminal.|
|>|This operator is a redirector - meaning that we can take the output from a command (such as using cat to output a file) and direct it elsewhere.|
|>>|This operator does the same function of the `>` operator but appends the output rather than replacing (meaning nothing is overwritten).|

Let's cover these in a bit more detail.  
  

## Operator "&"

This operator allows us to execute commands in the background. For example, let's say we want to copy a large file. This will obviously take quite a long time and will leave us unable to do anything else until the file successfully copies.

The "&" shell operator allows us to execute a command and have it run in the background (such as this file copy) allowing us to do other things!

  

## Operator "&&"

This shell operator is a bit misleading in the sense of how familiar is to its partner "&". Unlike the "&" operator, we can use "&&" to make a list of commands to run for example `command1 && command2`. However, it's worth noting that `command2` will only run if `command1` was successful.

  

## Operator ">"

This operator is what's known as an output redirector. What this essentially means is that we take the output from a command we run and send that output to somewhere else.

A great example of this is redirecting the output of the `echo` command that we learned in Task 4. Of course, running something such as `echo howdy` will return "howdy" back to our terminal — that isn't super useful. What we can do instead, is redirect "howdy" to something such as a new file!

Let's say we wanted to create a file named "welcome" with the message "hey". We can run `echo hey > welcome` where we want the file created with the contents "hey" like so:

![Pasted image 20230830163042.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830163042.png)

![Pasted image 20230830163056.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830163056.png)

_Note: If the file i.e. "welcome" already exists, the contents will be overwritten!_

  

## Operator ">>"

This operator is also an output redirector like in the previous operator (`>`) we discussed. However, what makes this operator different is that rather than overwriting any contents within a file, for example, it instead just puts the output at the end.

Following on with our previous example where we have the file "welcome" that has the contents of "hey". If were to use echo to add "hello" to the file using the `>` operator, the file will now only have "hello" and not "hey".

The `>>` operator allows to append the output to the bottom of the file — rather than replacing the contents like so:
![Pasted image 20230830163150.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830163150.png)

![Pasted image 20230830163123.png](/img/user/courses/tryhackme/linux_fandamentals/part_1/img/Pasted%20image%2020230830163123.png)

