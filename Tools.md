
# Tools used for evaluating device

## Kali Linux
“Kali Linux (formerly known as BackTrack Linux) is an open-source, Debian-based Linux distribution aimed at advanced Penetration Testing and Security Auditing. Kali Linux contains several hundred tools targeted towards various information security tasks, such as Penetration Testing, Security Research, Computer Forensics and Reverse Engineering.” (https://www.kali.org/docs/introduction/what-is-kali-linux/)
We chose Kali as it would include most tools we would need to perform tests and monitor the devices. Creating a bootable USB with the platform (https://www.kali.org/docs/usb/live-usb-install-with-windows/), we would have easy access to all of our tools without a designated linux machine.

## Nmap
“Nmap is a utility for network exploration or security auditing.” (https://www.kali.org/tools/nmap/#nmap)
We have used Nmap to discover the interfaces and ports that are open in the device. Having the device on the same network and access to its IP-address enables us to scan the device using this command:
```nmap -sC -sV -p- <IP>```
- sC: Script scan, scans for a default set of scripts to identify potential scripts that could be misused.
- sV: Service and Version Detection, scans the corresponding open port and reports what probable service is being used on the port.
- -p-: scans all 65535 ports

Output example:
![Screenshot_2022-03-22_11-17-25](https://user-images.githubusercontent.com/98017528/159465247-7c69ae95-9645-47d6-9ed9-79caa135f1f5.png)
## Wireshark

## Burp Suite

## Binwalker

## Ettercap
