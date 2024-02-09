---
{"dg-publish":true,"permalink":"/courses/tryhackme/bash-scripting/content/parameters/","dgPassFrontmatter":true,"noteIcon":""}
---

We will now look at one of the main features of bash and that's using parameters.

  

We will firstly  look at parameters specified using the command line when running the file. These come in many forms but often have the "$" prefix because a parameter is still a variable.

Lets start by declaring a parameter that is going to be our first argument when running our bash script.

![Pasted image 20230831191857.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831191857.png)

We now run our script with `./example.sh Alex`

And sure enough we get returned with “Alex”

So what if we wanted the 2nd argument? Well the process is very simple and we simply add a `$2` instead of `name=$1`

Then run with `./example.sh Alex Tony`

What do you think it would return?

And it would return "Tony".

What if we didn't want to supply them like this however, and instead it would let us type in our name in a more interactive way, we can do this using `read`.

![Pasted image 20230831191925.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831191925.png)  

This code will hang after its ran, this gives you the opportunity to type in your name.

![Pasted image 20230831191941.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831191941.png)

And we can see that it worked!  

Maybe try making a little biography maker, where you take the name, age, and job as parameters. Store them inside a variable and then output them to the screen inside a sentence. 

However there is so much more that you can do with parameters and I advice you to play around with them, after all practice is what makes you better! 

Answer the questions below

How can we get the number of arguments supplied to a script?

answer: $#

How can we get the filename of our current script(aka our first argument)?

answer: $0

How can we get the 4th argument supplied to the script?  

answer: $4 

If a script asks us for input how can we direct our input into a variable called ‘test’ using “read”

answer: read test 

What will the output of “echo $1 $3” if the script was ran with “./script.sh hello hola aloha”

answer: hello aloha 
