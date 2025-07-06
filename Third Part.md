# Linux Bash: Vulnerability Scan of the Local Network

Objective: Use Linux Bash to perform a vulnerability scan of the local network and automate it with a cron job.

Task:
1. Write a Bash script that:
   - Scans your local network to find open TCP ports and detects OS versions on each host.
   - Displays the results in a readable format on the screen.
   - consider using `nmap`.

2. Automation: Schedule this script to run daily at 4 pm using `cron`.
   - Edit the crontab with `crontab -e` and add a new cron job to run the script.
  

## Task 1
This really took my time, the script was not running because there some kind of error in my typing...<br>
so I did some simple nmap scanning first in the terminal. And then I used the leafpad. <br>
The one in leafpad was from ChatGPT for testing but it was complicated and so I tried a normal nmap syntax that includes the open ports and OS versions. Added echo to know where things stopped and go. <br>
Had to label from nmap --help so I couldn’t forget what to use.

![image](https://github.com/user-attachments/assets/c40542e2-96e4-4ee7-9262-798a199c03fd)<br>

So this did not work the first time because, for some reason, when I saved it as a .sh, it converted to Windows style line endings. <br>
It was not recognizing that the spaces and line breaks and kept erroring. Also realized I mistyped the ip too. (From the ChatGPT sample)

![image](https://github.com/user-attachments/assets/17508905-3f3a-435e-aa86-3a48c020e39b)

I searched online and I needed to convert the file to unix base, which then worked.
![image](https://github.com/user-attachments/assets/d23f52ed-1bb6-4fda-aa39-d75a1abcd9ad)
![image](https://github.com/user-attachments/assets/92da86b2-1dac-46db-9245-4472a56f3812)
![image](https://github.com/user-attachments/assets/8b686807-995b-41d1-a14a-546d7f1cd120)
![image](https://github.com/user-attachments/assets/6283711a-c4d5-46b6-a766-6ae36996599b)

## Task 2
For Cron
![image](https://github.com/user-attachments/assets/2e9c7b86-ac09-4ca0-816e-d739a4582c7a)
verifying but it looks just like it, so I decreased the comments and it worked.
![image](https://github.com/user-attachments/assets/b5b199e7-e5ac-4f24-a19a-0cb57f375a1b)

## Final Output
![image](https://github.com/user-attachments/assets/30cce270-a718-43a6-8369-288ee7e0e8a9)
![image](https://github.com/user-attachments/assets/2cf4154d-6888-4348-b0f1-eb36ed9f080a)
![image](https://github.com/user-attachments/assets/9cb378a9-96cb-4207-806e-92eaa7e0a6c9)
![image](https://github.com/user-attachments/assets/fbdd4004-485a-40c6-ab8b-7bdabfc9748c)




