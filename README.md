# Home Lab Setup

## Objective

This Home Lab project was aimed to set up and configure a personal cybersecurity home lab using VirtualBox, utilizing Ubuntu and Kali Linux virtual machines. The goal was to gain hands-on experience with key cybersecurity tools, including Wireshark for packet analysis and nmap for vulnerability scanning. This project enhanced my understanding of many key areas and tools of cybersecurity, including virtual machines, penetration testing, and ethical hacking techniques in a sandbox environment.

### Skills Learned

- Network traffic analysis to interpret various protocols (TCP, UDP, ICMP).
- Firewall configuration through command line (ufw)
- Penetration testing to perform network scans to detect open ports.
- Ability to configure and manage virtual machines for a simulated environment.
- Exposure to new operating systems such as Ubuntu and Kali Linux.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Virtualization software (VirtualBox) for creating and configuring virtual machines.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.
- Penetration testing tools (nmap) to run a network scan.

## Steps
First, I downloaded VirtualBox as well as ISO files for Ubuntu and Kali Linux.

I then created two virtual machines through VirtualBox using the ISO files. This way, I could simulate network attacks using Kali Linux as the attacker and Ubuntu as the defender.

*Ref 1: VirtualBox VMs*

<img width="400" alt="Screenshot 2024-12-16 at 4 41 09 PM" src="https://github.com/user-attachments/assets/93b02ea0-ee44-4b91-b04f-e14275f8b7e5" />


Next, I needed to create a network so that my 2 VMs could communicate. Through VirtualBox, I created a NAT Network and connected both VMs to it.

*Ref 2: Network Diagram*

<img width="400" alt="Screenshot 2024-12-17 at 7 16 06 PM" src="https://github.com/user-attachments/assets/9d358bf5-dd05-447b-81ae-8e0c92e7d777" />


I updated both systems, and my next step was to configure the Ubuntu firewall to allow communication from Kali. Using the command line, I set up the firewall to allow all communication from the IP address of my Kali Linux VM. 

*Ref 3: Firewall Configuration*

<img width="800" alt="Screenshot 2024-12-17 at 7 37 21 PM" src="https://github.com/user-attachments/assets/ae2e8ef2-49a8-486c-b7f8-49fd10ab9e2e" />


I installed the Wireshark software on Ubuntu, which I would use to log and analyze the network traffic. Now, I was ready to begin testing.

On my Kali Linux machine, I simulated an attack on the Ubuntu machine using 'nmap -A [Ubuntu VM IP]'. This performed a detailed scan of the Ubuntu system, including open/closed ports, traceroute, OS detection, etc. 

On my Ubuntu machine, Wireshark captured and logged all of this traffic from the attack, so I was then able to view and analyze all of the packets sent and received, including TDP, UDP, and ICMP in order to see what ports on my system were open/closed and could detect vulnerabilities.

*Ref 4: Attack Simulation Results*

<img width="800" alt="Screenshot 2024-12-17 at 7 40 42 PM" src="https://github.com/user-attachments/assets/12eb5c60-281d-438d-a787-9f9aa62019f2" />
