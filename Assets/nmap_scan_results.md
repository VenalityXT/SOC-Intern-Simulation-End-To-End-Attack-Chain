README Section: Nmap Scan and Analysis
Purpose:
To perform reconnaissance and identify open ports and running services on the target machine (Metasploitable 2) using Nmap.

Command used:
bash
Copy
Edit
nmap -sS -A 192.168.56.102
-sS (SYN scan):
Performs a stealthy TCP SYN scan by sending SYN packets and analyzing responses. It’s less likely to be logged by simple intrusion detection systems because it doesn't complete the TCP handshake.

-A (Aggressive scan):
Enables OS detection, version detection, script scanning, and traceroute. This provides detailed info about the target system beyond just open ports.

Scan Results Summary:
Port	Service	Version/Details	Notes / Possible Vulnerabilities
21/tcp	FTP	vsftpd 2.3.4 - Anonymous FTP login allowed	Potential exploit: Backdoor in vsftpd 2.3.4 (classic Metasploitable vuln)
22/tcp	SSH	OpenSSH 4.7p1	Older SSH version, possible brute force or known exploits
23/tcp	Telnet	Linux telnetd	Insecure cleartext protocol; possible weak creds
25/tcp	SMTP	Postfix smtpd with SSLv2 support	SSLv2 is insecure, potential for downgrade attacks
53/tcp	DNS	ISC BIND 9.4.2	Outdated DNS server version
80/tcp	HTTP	Apache 2.2.8	Default web server with potentially outdated software
139/445	SMB	Samba smbd 3.x	Possible misconfigurations, weak authentication
1524/tcp	Bind shell	Metasploitable root shell	Known open root shell backdoor in Metasploitable
3306/tcp	MySQL	MySQL 5.0.51a	Default database, potentially weak credentials
5432/tcp	PostgreSQL	PostgreSQL 8.3.0	Default DB with potential weak configs
5900/tcp	VNC	VNC protocol 3.3	Unsecured remote desktop, possible weak auth
6667/tcp	IRC	UnrealIRCd 3.2.8.1	Known vulnerable IRC server versions
8180/tcp	HTTP	Apache Tomcat 5.5	Vulnerable Java web server

What this means for your SOC simulation:
Vsftpd 2.3.4 on FTP port 21 allows anonymous login, a classic Metasploitable vulnerability with a known backdoor exploit.

Telnet and FTP are unencrypted protocols allowing interception or credential capture.

Bind shell on port 1524 is an open backdoor shell providing root access.

Multiple outdated services (SSH, Samba, Apache, MySQL, PostgreSQL) provide opportunities for exploitation.

The presence of various services simulates a realistic vulnerable host for detection and response scenarios.

Next Step Suggestion:
Start with the classic vsftpd 2.3.4 backdoor exploit to gain an initial foothold, then simulate lateral movement and privilege escalation from there.
