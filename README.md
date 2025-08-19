# CMD Network Troubleshooting Guide
This guide demonstrates how to use basic **Command Prompt (CMD) network commands**
## 1. Open Command Prompt
- Press **Windows Key + R**
- Type 'cmd' then **Enter**
- Screenshot :
- ![Open CMD](screenshots/screenshot_blankcmd.jpg)
---
## 2. Check Your IP Configuration
- Open Command Prompt
- Type 'ipconfig /all' then **Enter**
- Displays IP address, Subnet mask, Default Gateway, DNS Servers.
- Useful for checking if your device has a valid network setup.
- Screenshot:
  ![IP Config](screenshots/ipconfig_all.jpg)
  ---
## 3. Test Connectivity with Ping
- Open Command Prompt
- Type ping google.com
- This confirms if your computer can reach the internet.
- Replies mean it is working, timeouts mean problem
- Screenshot:
![Ping Test Success](screenshots/pinggoogle.jpg)
![Ping Test Failure](screenshots/failedping.png)
---
## 4. Trace the Route to a Website
- Open Command Prompt
- Type tracert google.com
- This shows the "hops" meaning how many hops it takes data to reach destination.
- Helps identify where delays or blocks happen.
- Screenshot:
![Tracert](screenshot/tracert)
---
## 5. Test DNS Resolution
- Open Command Prompt
- Type nslookup google.com
- Displays which DNS server is being used.
- Shows the resolved IP address for the domain.
- Screenshot:
![NSlookup](screenshots/nslookup.png)
## 6. View Active Network Connections
- Open command prompt
- Type nestat -ano
- Lists active connections, listening ports, and process IDs.
- Help detect open connections or suspicious activity.
- Screenshot:
![Netstat](screenshots/netstat)
---
## 7. Flush and Renew IP Address
- Open Command Prompt
- Type ipconfig /release (this releases the current IP)
- Screenshot: ![IP Release](screenshots/ipconfigrelease.png)
- Then type ipconfig /renew (this fixes issues with DHCP and IP conflicts)
- Screenshot:
![IP Renew](screenshots/ipconfigrenew.png)
## 8. Clear DNS Cache
- Open Command Prompt
- Type ipconfig /flushdns
- This clears stored DNS entries and helps resolve issues when sites fail to load properly.
- Screenshot:
![Flush DNS](screenshots/ipconfigflushdns.png)
