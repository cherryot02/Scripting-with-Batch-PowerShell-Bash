# Introduction
> Welcome to my very basic-looking script lab work. <br>

Before I get into it, I will do some introduction and list the things I used. <br><br>

This lab was done in virtual machines running in the Virginia Cyber Range so I could only really use the OS the was being used in class, <br> 
but you can very much run these in any recent systems.

We are mainly using:
<ol>
  <li>Windows 7 for Batch and PowerShell (This was our target system so we just used this anyway.) </li>
  <li>Kali Linux</li>
</ol>

>[!CAUTION]  
>Be careful though, because you have to know how what each line does, <br>
>if not, well you may have a keylogger now and you won't know it.<br>
>I'm kidding, but this warning applies to every script you'll find in the internet.

Main objectives of this lab:
<ul>
  <li>Develop skills in Windows Batch & PowerShell, and Linux Bash scripting.</li>
  <li>Practice network recon and system process monitoring.</li>
  <li>Set up automated tasks with cron on Linux.</li>
  <li>Work with commonly available AI assistants</li>
</ul>

You saw that right. <em>AI</em>. 🫢 <br>
This may or may not be vibe scripting but you will find out. <br>
<br>

Alright kidding aside, these tasks were given in class and we are meant execute them ourselves <br>
So "using AI" was permitted but it did not really help me that much because it would output too many complicated stuff that was unneccessary.


# First Part: Windows Batch File - Local Network Ping Sweep

Write a Windows Batch file that: <br>
   - Loops through a range of IP addresses on your local network (e.g., `192.168.1.1` to `192.168.1.254`).
   - Pings each IP address once.
   - Displays reachable IP addresses on the screen.
> HINT: Use a `FOR` loop and the `ping` command to iterate through IP addresses.


## My Process and output
I had a bit of a hard time; I first tried and see what ChatGPT has to say but I did not understand the syntax and it did not output properly <br>
so I started to do it manually first to see if the normal commands are working.  <br>
I was not able to screenshot the first one and I learned that the comments for this “::” and not “#”.  <br><br>
![image](https://github.com/user-attachments/assets/e15056aa-624d-4690-9c5b-04511a4d8461) <br><br>
I did realize that I wasn’t supposed to run this in the terminal and needed to use a text editior.<br><br>

Also pinged the linux machine which was reachable.<br>
So I then tried the script from the presentation(powerpoint) and adjusted some bits accordingly.<br>
At this point, I realized that I must use the notepad so this could run and save it as “filename.bat”…<br>
this was the result:<br><br>

![image](https://github.com/user-attachments/assets/2fc0181e-3224-4e3c-8b1f-188ac0e36422)<br><br>
So now, I’ll do it with the instructions and instead of a separate file for the output, <br>
I will just echo it to the terminal. I did leave an else for the unreachable just to see, <br><br>

![image](https://github.com/user-attachments/assets/a3a7e721-999f-450c-a7ea-fa61313afc3b)<br><br>

Only a few popped out alive and I did not wait for it to finish so I will remove the unreachable ones so it’s easier to see.
![image](https://github.com/user-attachments/assets/7c10e89d-f798-46fd-b328-bcb0f1e1efe2) <br><br>

As soon as the Ping sweep was complete, the terminal closed. Replaced the word alive to “reachable” for the instructions and changed timeout to -w 500 so it’s faster. <br><br>
![image](https://github.com/user-attachments/assets/d34280a6-8abf-4d0c-a226-bf630cb9a504)





