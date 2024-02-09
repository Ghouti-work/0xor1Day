---
{"dg-publish":true,"permalink":"/courses/tryhackme/bash-scripting/content/variables/","dgPassFrontmatter":true,"noteIcon":""}
---

Now we are moving onto variables, in bash these are quite simple and we create them like so:

![Pasted image 20230831152517.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152517.png)  

Where we give the value of `Jammy` and assign it to the variable `name`.

Please note that for variables to work you cannot leave a space between the variable name, the ”**=**” and the value. They cannot have spaces in.

So how would we now use our variable? Well its also very simple.

  

We have to add a `$` onto front of our variable name in order to use it.

![Pasted image 20230831152532.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152532.png)  

If we test this out in our own terminal we get something like this:

`$ name="Jammy"`

`$ echo $name`

`Jammy`  

This would output “**Jammy**” to the screen.

Variables make it much easier to store data and rather than typing out the same thing in multiple places we could simply insert our variable with $var and then declare that to a certain value making it easier to fall back on if you do something wrong and need to change it. So how can we debug our code?

Debugging is a very important part of programming so we should get used to problem solving and fixing errors as early as possible. And bash has a few built in features that make our life simple.

When running at the command line you can do:

`bash -x ./file.sh`

You can make a simple bash script(now you know some basic syntax) and make something completely wrong. Then step through your program with debug mode and see what it looks like when it throws errors!

This tells you which lines are working and which lines are not. If you want to debug at a certain point you can insert `set -x` into your script and `set +x` to end the section like the following:

![Pasted image 20230831152615.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152615.png)  

So lets look at an example. This is our script from earlier being ran with `bash -x ./example.sh`

![Pasted image 20230831152630.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152630.png)  

You can see its outputting a **+** for the command and then the output of what that command executed. If there was an error it would output a **-** on that line this makes it easy to spot where you have gone wrong so you can fix them.

We can also use multiple variables in something like an echo statement. You aren't just limited to using 1!

![Pasted image 20230831152646.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152646.png)

Answer the following questions and use this piece of code to guide you.

![Pasted image 20230831152706.png](/img/user/courses/tryhackme/Bash%20Scripting/content/img/Pasted%20image%2020230831152706.png)  

### Answer the questions below

What would this code return?

answer: Jammy is 21 years old

How would you print out the city to the screen?

answer: echo $city 

How would you print out the country to the screen?

answer: echo $country
