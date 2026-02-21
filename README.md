# Pen-testing

## 📌 About This Project

The Digital Investigation and E-Discovery project is an academic cybersecurity assessment demonstrating a practical penetration testing attack using the Metasploit Framework, showcasing anti-forensic techniques, backdoor injection methods, and digital forensic investigation procedures within a controlled laboratory environment using Kali Linux as the attacking platform and Windows Server 2022 as the target system.

---

## Technologies Used

**Hardware:** Kali Linux Virtual Machine (VirtualBox), Windows Server 2022 Target System, Host Network Interface for inter-VM communication

**Software:** Metasploit Framework v6.4, msfvenom Payload Generator, Meterpreter Post-Exploitation Agent, WinRAR SFX Archive Tool, TightVNC Remote Desktop Viewer, TCPView Network Monitoring Tool, VirusTotal Online Malware Scanner

**Attack Techniques:** Steganography via SFX Archive, Reverse TCP Shell, Social Engineering via Phishing Email, Process Migration, Event Log Tampering

---

## Key Features Developed

**Payload Creation and Delivery:** A functional Windows reverse TCP Meterpreter payload was generated using msfvenom, configured to establish a covert connection back to the attacker machine on IP 192.168.1.65 over port 4444, packaged as a self-extracting executable disguised as a legitimate World Cup ticket image.

**Data Hiding and Steganography:** The malicious payload was concealed within an SFX archive configured with silent extraction mode, a custom ticket-themed icon, and automatic execution upon opening, making the file visually indistinguishable from a legitimate image download to an untrained user.

**Social Engineering Attack Vector:** A convincing phishing email campaign was simulated, delivering the malicious payload via a Google Drive hosted link embedded within a fabricated World Cup Final ticket giveaway notification, exploiting urgency and reward-based psychological triggers.

**Post-Exploitation and Surveillance:** Upon successful exploitation, the attacker demonstrated full remote control capabilities including live desktop monitoring via VNC, real-time screensharing, screenshot capture, filesystem navigation, and sensitive data exfiltration from the victim machine.

**Anti-Forensic Techniques:** Process migration from the original payload process (PID 3224) to a legitimate system process (PID 900) was performed to evade detection, followed by complete Windows Event Log erasure using the Meterpreter clearev command, eliminating 791 application log records.

**Digital Forensic Investigation:** The victim's compromise was systematically investigated through Task Manager CPU analysis, Resource Monitor network activity tracking, Windows Event Viewer log tampering identification, VirusTotal malware confirmation, netstat network connection analysis, and TCPView attacker IP identification.

---

## Project Outcomes

Successfully demonstrated a complete attack lifecycle from initial payload creation through social engineering delivery, active exploitation, post-exploitation data theft, anti-forensic evasion, and subsequent victim-side digital investigation, providing a comprehensive practical understanding of both offensive and defensive cybersecurity disciplines.

Conducted in-depth analysis of two real-world threat actor campaigns, the APT29 ROOTSAW diplomatic phishing operation and the BlackTech firmware backdoor attack targeting Cisco routers, contextualising the laboratory demonstration within the broader landscape of contemporary advanced persistent threat activity.

Established a thorough countermeasures framework addressing endpoint protection, network security hardening, email filtering, user awareness training, incident response planning, and forensic preparedness, grounded directly in the attack vectors observed and exploited throughout the practical demonstration.
