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

