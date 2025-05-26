# Scan Your Local Network for Open Ports
**. Objective:** Learn to discover open ports on devices in your local network to understand network exposure.

**. Tools:** Nmap (free), Wireshark (optional)

## 1. Install Nmap from official website

nmap is pre installed tool in kali for check run this command

> nmap -h
> 

![](https://miro.medium.com/v2/resize:fit:679/1*41O1V-nwc4XgbJSSRD63gA.png)

## 2.Find your local IP range command;

> ip a
> 
> 
> ifconfig
> 

![](https://miro.medium.com/v2/resize:fit:700/1*3XP9ZBSIPfTThKnkqf7jHA.png)

## 3.Run: nmap -sS 192.168.1.0/24 to perform TCP SYN scan

![](https://miro.medium.com/v2/resize:fit:700/1*Nk5aSuAMpNz78w2ghfWPrA.png)

## 4.Note down IP addresses and open ports found.

**. Detailed Results :**

192.168.117.1

All 1000 scanned ports are filtered

This means no response was received — likely due to a firewall blocking the scan

192.168.117.2

Port 53/tcp is filtered — this port is typically used for DNS (Domain Name System)

The remaining 999 ports are closed, which means the system received the request but actively rejected the connection

192.168.117.254

All 1000 scanned ports are filtered

This is most likely a router or firewall-protected device that blocks incoming scan requests

192.168.117.128 (Your own system)

All 1000 scanned ports are closed

This indicates that the scan reached the system, but all ports rejected the connection attempts

## 5.Optionally analyze packet capture with Wireshark

![](https://miro.medium.com/v2/resize:fit:1000/1*gducjjxJEHNpvril4Ck23A.png)

## 6.Research common services running on those ports.

there is no services running because off no port is running

## 7.Identify potential security risks from open ports.

i have nothing found suspicious on this services because off no port is open

## 8.Save scan results as a text or HTML file.

here i save these output in test file like nmap.txt

comand;

> nmap -sS 192.168.117.0/24 -oN nmap.txt
> 

![](https://miro.medium.com/v2/resize:fit:700/1*RUnezPWgospTJqZ-EZ8m_w.png)

scan of result in nmap.txt file

![](https://miro.medium.com/v2/resize:fit:700/1*cFGHJ6OYng6Q_DWlkI-zzA.png)
