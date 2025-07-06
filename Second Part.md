# Second Part: Windows PowerShell - Processes and network connections

Write a PowerShell script to monitor current processes and network connections.
   - Lists all active processes on the machine.
   - Shows current network connections, including IP addresses, protocol, and state.

> Hint: Use `Get-Process` for active processes and `Get-NetTCPConnection` (or `netstat`) for network connections.<br>


First we'll have to open a web browser and visit three different websites. <br>
The reason why we are doing this is because we need to see open connections easier by sending and receving traffic via the public internet.

After visiting the website, I first ran the cmdlets on its own to check if their working right then proceeded with the task. <br>
Then used notepad and saved as a .ps1 file for PowerShell, It said I need to run a genuine windows so I switched to the PowerShell ISE. <br><br>

I learned that Write-Host is the “echo” equivalent. And # for comments this time. <br>
They are not recognizing `Get-NetTCPConnection` so I will try netstat. <br>
I searched and it’s because Get-NetTCPConnection works on Windows 8 and above…<br><br>
Also replaced the Select-Object according to instructions.  <br><br>
![image](https://github.com/user-attachments/assets/6186278d-86d4-4c80-8a49-08e14f623ec1)

![image](https://github.com/user-attachments/assets/2b75b308-de1a-45c6-aa1e-a2b4f0867e42)

Get-Process had no problems but now it’s not outputting any network connections:
![image](https://github.com/user-attachments/assets/766d9a6a-b47e-468c-8d9a-5532eb87093f)

Turns out, I must run the actual netstat first and then display the output accordingly. <br>
I got stuck here for a while and asked ChatGPT, but it was not working right, and it got complicated.
![image](https://github.com/user-attachments/assets/308d7aa4-6066-4e0c-878f-8979ea32aa0f)

So cleared everything trial and errored a lot, and then ended up removing -an there and made everything simpler by just doing this. 
![image](https://github.com/user-attachments/assets/744ade4f-347a-492b-a109-d3e20b19b92a) <br>
I searched for the proper syntax and got it here at 3:53 (https://www.youtube.com/watch?v=lgginAiOEXo) and compared it with the presentation.<br>

![image](https://github.com/user-attachments/assets/ce507031-a15a-45ad-9122-aa46736c8a50)
output was this so now I’ll visit some websites and run the script again. <br>
It took a while for the output to finish though, but the headers gone.
![image](https://github.com/user-attachments/assets/08aec384-8634-4ecc-9dee-386b12a3a470)

I wanted the header/labels but there’s probably a better way to do this.  <br>
ChatGPT did this and it’s basically just organizing the output…
![image](https://github.com/user-attachments/assets/cc4434ec-5dde-4315-b817-8312370fb2f2)

# Next
[Third Part](https://github.com/cherryot02/Scripting-with-Batch-PowerShell-Bash/blob/main/Third%20Part.md) Linux Bash Scripting, first part.




