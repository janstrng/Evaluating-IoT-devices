
# Tools used for evaluating devices

## Testing enviornment
The environment the tests are performed in are set up using a computer acting as a router using it as a hotspot or proxy. This way we will be able to easily gather the data that is being transported from the devices.  
A secondary computer running Kali, also connected to the hotspot, acts as an attacker attempting to gain access or control over the device. The reason why we used a hotspot and not a dedicated network was because we used the normal campus network, and it would be difficult to filter traffic.

We would strongly recomend using Linux based operating systems because there are more tools made for it, and it will make it easier to test the devices.

Our setup was not ideal, we would have liked to have had a dedicated network and router. 

In our opinion the ideal setup would include the following:
- Dedicated network
- Router
- Two computers, where atleast one of them are running Kali
- All of the programs listed beleow


## Kali Linux
![kali](https://user-images.githubusercontent.com/98017528/159913136-72ea965a-3430-41c5-932d-ab37b8b7999e.png)
“Kali Linux (formerly known as BackTrack Linux) is an open-source, Debian-based Linux distribution aimed at advanced Penetration Testing and Security Auditing. Kali Linux contains several hundred tools targeted towards various information security tasks, such as Penetration Testing, Security Research, Computer Forensics and Reverse Engineering.” [^1]
We chose Kali as it would include most tools we would need to perform tests and monitor the devices. Creating a bootable USB with the platform [^2], we would have easy access to all of our tools without a designated linux machine.

## Nmap
“Nmap is a utility for network exploration or security auditing.” (https://www.kali.org/tools/nmap/#nmap)
We have used Nmap to discover the interfaces and ports that are open in the device. Having the device on the same network and access to its IP-address enables us to scan the device using this command:  
```nmap -sC -sV -p- <IP>```
- sC: Script scan, scans for a default set of scripts to identify potential scripts that could be misused.
- sV: Service and Version Detection, scans the corresponding open port and reports what probable service is being used on the port.
- -p-: scans all 65535 ports

Example of output:
![Screenshot_2022-03-22_11-17-25](https://user-images.githubusercontent.com/98017528/159465247-7c69ae95-9645-47d6-9ed9-79caa135f1f5.png)

After finding what interfaces are open in the device and further research and evaluation of the necessity and security  of the service that is being used.
The evaluation is taken into consideration when testing the security of the [interfaces](https://github.com/janstrng/Evaluating-IoT-devices/blob/main/Framework.md#interfaces) of the device.


## Wireshark
Wireshark is a network protocol analyzer. It is used by organizations, governments and educational institutions around the globe. We chose Wireshark because it is one of the most used tools for network analysis in the world, and therefore there would be more tutorials and resources.
![wireshark](https://user-images.githubusercontent.com/98017528/159920105-bd147713-f39a-4c41-8339-2ee758d05d3e.png)
Using wireshark on the computer running a hotspot, we would be able to see the traffic sendt between the phone and device, towards the server. Analyzing the packages sendt, we can observe what protocol is being used and what data is being transfered.  
In most of our tests, we found that the packages had been encrypted, mostly by the use of Transport Layer Security (TLS).


Wireshark works on all the common operating systems[^3]. That gives us flexibility, and another reason as to why we chose to use it.

## Burp Suite
Burp Suite is a graphical tool that lets you test web applications.
![burp](https://user-images.githubusercontent.com/98017528/159920099-27b1463c-b8e9-4c1c-b910-ae2757342313.png)

Using burp suite we can analyze the packets that are being sent towards relevant services of the device.  
In our case we found a web-server on a device hosting an API towards the device. We could then use proxy and interception see how the web-requests were structured and how requests were sent.

## Binwalker
"Binwalk is a tool for searching a given binary image for embedded files and executable code. Specifically, it is designed for identifying files and code embedded inside of firmware images." [^4] 
Given that the firmware of the device is available, binwalker can be used to inspect the embedded files for hardcoded values associated with authentication. 
![binwalk](https://user-images.githubusercontent.com/98017528/159920094-c4717241-90d2-43e0-933a-fbefe1d6b4de.png)

Having gained access to a devices firmware we now can use binwalk to extract files from the .bin file.  
We can start by analyzing the firmware using:   
```binwalk <firmware-image>```  

From there we can extract known file types:  
```binwalk -e <firmware-image>```  

Going into the extracted file (formated as "_filename.extracted") we found ourself limited to what we could find due to encrypted zip-files and non-humanreadable text, witch might indicate a level of protection and security.

## Ettercap
"Ettercap is a comprehensive suite for man in the middle attacks. It features sniffing of live connections, content filtering on the fly and many other interesting tricks. It supports active and passive dissection of many protocols and includes many features for network and host analysis." [^5]. 
![ettercap](https://user-images.githubusercontent.com/98017528/159920102-4bead2dd-4aba-403d-a41e-f9cf35d97fcf.png)

We were recommended Ettercap by our supervisor as a great tool to use for MitM attacks. 

The way we used Ettercap was with arp poisoning, and then used Wireshark and the ARP table. This is a Man-in-the-Middle attack. We followed a [guide](https://pentestmag.com/ettercap-tutorial-for-windows/) for Man-in-the-middle attacks. Ettercap is already installed as a package on Kali. 

NB! Ettercap is only compatible with Linux based OS.

## SQL injection
Testing the application for SQL-vulnerabilities we attempted injecting the text-fields of the login-page, checking for common SQL strings such that are found here: [W3schools](https://www.w3schools.com/sql/sql_injection.asp/) .
If ending up, getting an SQL-error or actually succeeding logging in, will result in a fail for the application.
Not finding anything that indicates the application to be vulnerable, such as wrong credentials- or format-message, passes the test on point A.4 and  A.5.

Scource:
[^1]: https://www.kali.org/docs/introduction/what-is-kali-linux/
[^2]: https://www.kali.org/docs/usb/live-usb-install-with-windows/
[^3]: https://www.wireshark.org/
[^4]: https://www.kali.org/tools/binwalk/
[^5]: https://www.ettercap-project.org/
