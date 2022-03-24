
# Tools used for evaluating devices

## Testing enviornment
The environment the tests are performed in are set up using a computer acting as a router using it as a hotspot or proxy. This way we will be able to easily gather the data that is being transported from the devices.  
A secondary computer running Kali, also connected to the hotspot, acts as an attacker attempting to gain access or control over the device.


## Kali Linux
![kali](https://user-images.githubusercontent.com/98017528/159913136-72ea965a-3430-41c5-932d-ab37b8b7999e.png)
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

After finding what interfaces are open in the device and further research an evaluation of the necessity of the service that is open.
The evaluation is taken into consideration when evaluating the [interfaces](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#interfaces) of the device.



## Wireshark
Wireshark is a network protocol analyser. It is used by organizations, governments and educational institutions around the globe. We chose Wireshark because it is one of the most used tools for network analysis in the world, and therefore there would be more tutorials and cookbooks on it.
![wireshark](https://user-images.githubusercontent.com/98017528/159920105-bd147713-f39a-4c41-8339-2ee758d05d3e.png)

In addition, we were recommended to Wireshark by our supervisor. The method we used Wireshark was to monitor traffic from the DUT. 	
## Burp Suite
![burp](https://user-images.githubusercontent.com/98017528/159920099-27b1463c-b8e9-4c1c-b910-ae2757342313.png)


## Binwalker
"Binwalk is a tool for searching a given binary image for embedded files and executable code. Specifically, it is designed for identifying files and code embedded inside of firmware images." (https://www.kali.org/tools/binwalk/)  
Given that the firmware of the device is available, binwalker can be used to inspect the embedded files for hardcoded values associated with authentication. 
![binwalk](https://user-images.githubusercontent.com/98017528/159920094-c4717241-90d2-43e0-933a-fbefe1d6b4de.png)

## Ettercap
"Ettercap is a comprehensive suite for man in the middle attacks. It features sniffing of live connections, content filtering on the fly and many other interesting tricks. It supports active and passive dissection of many protocols and includes many features for network and host analysis." (https://www.ettercap-project.org/). 
![ettercap](https://user-images.githubusercontent.com/98017528/159920102-4bead2dd-4aba-403d-a41e-f9cf35d97fcf.png)

We were recommended Ettercap by our supervisor as a great tool to use for MitM attacks. 

