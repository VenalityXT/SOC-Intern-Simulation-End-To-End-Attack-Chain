# SOC Intern Simulation – End-to-End Attack Chain and Security Response

![Insert Image Here – Attack Chain Diagram or Lab Architecture]

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Objectives](#objectives)
- [Key Achievements](#key-achievements)
- [Skills Demonstrated](#skills-demonstrated)
- [Repository Structure](#repository-structure)
- [Recommendations for Future Enhancements](#recommendations-for-future-enhancements)
- [License](#license)

---

## Project Overview

This lab replicates a real-world SOC intern experience by simulating a complete attack lifecycle—from phishing to lateral movement and privilege escalation—across a controlled virtual network. Using open-source tools like **Wazuh** or the **ELK Stack**, the project focuses on threat detection, incident response, alert enrichment, and developing actionable security documentation and awareness training.

---

## Technologies Used

- **ELK Stack** or **Wazuh** – SIEM for log aggregation, correlation, and visualization
- **Metasploit/Kali Linux** – Attack simulation for exploitation and persistence
- **Windows Sysmon** – Endpoint logging for detecting malicious activity
- **MITRE ATT&CK Navigator** – Mapping attacks to the ATT&CK framework
- **Python/PowerShell** – Scripting for automation and alert enrichment
- **Phishing Simulation Tools** – For creating and deploying phishing payloads

---

## Objectives

- **Simulate a complete attack chain**: Track an attack from phishing through privilege escalation
- **Use open-source tools for detection and response**: Set up Wazuh or the ELK Stack for monitoring and alerting
- **Document the full incident response lifecycle**: From detection to remediation
- **Develop security awareness training materials**: Including phishing prevention and incident response education
- **Create SOC workflows and SOPs**: Standard Operating Procedures for incident handling

---

## Key Achievements

- **End-to-End Attack Simulation:**  
  *Executed a full cyber kill chain, including phishing, persistence, and lateral movement, using Kali Linux and Metasploit across a Windows lab environment.*

- **Real-Time Detection with ELK/Wazuh:**  
  *Monitored logs from compromised endpoints using ELK Stack or Wazuh to detect anomalies and pivot across attack stages.*

- **Mapped to MITRE ATT&CK:**  
  *Aligned each attack phase with relevant MITRE ATT&CK techniques for improved detection logic and threat modeling.*

- **Developed SOC Workflows:**  
  *Created analyst-ready Standard Operating Procedures (SOPs) and simulated triage/escalation workflows.*

- **Built Awareness Materials:**  
  *Produced security awareness content and phishing simulation templates for employee training use cases.*

---

## Skills Demonstrated

- **SIEM & Security Monitoring:**  
  *Configured Wazuh or ELK Stack to collect, normalize, and visualize log data from Windows and Linux systems.*

- **Incident Response & Threat Detection:**  
  *Tracked attacker behaviors through the full kill chain and documented step-by-step response actions.*

- **Threat Intelligence Enrichment:**  
  *Identified and contextualized IOCs using online threat feeds and MITRE ATT&CK Navigator.*

- **Scripting & Automation:**  
  *Wrote Python and PowerShell scripts to enrich alerts, extract indicators, and automate evidence gathering.*

- **Security Awareness & Documentation:**  
  *Created phishing education materials, incident response SOPs, and after-action reports.*

- **Network & Endpoint Security:**  
  *Designed and defended a segmented network with hardened Windows endpoints and basic firewall rules.*

---

## Repository Structure
```
SOC-Intern-Simulation/

├── attack_simulation/
│ ├── phishing_payloads/ # Phishing payload scripts and resources
│ ├── metasploit_scripts/ # Metasploit attack scripts for privilege escalation
│ └── MITRE_mapping.md # MITRE ATT&CK mapping for each attack phase

├── detection_response/
│ ├── ELK_Wazuh_configs/ # ELK or Wazuh configuration files
│ ├── IOC_enrichment_scripts/ # Python/PowerShell scripts for enriching IOCs
│ └── incident_report.md # Incident response documentation for this lab

├── documentation/
│ ├── SOPs/ # Standard Operating Procedures for SOC response
│ ├── security_awareness_materials/ # Phishing education materials and presentations
│ └── lessons_learned.md # After-action report, lessons learned

└── assets/
├── image_storage.md

├── README.md
└── LICENSE
```

---

## Recommendations for Future Enhancements

- **Integrate SOAR tools** (like Shuffle or TheHive) for automated incident response
- **Include lateral movement detection** via PowerShell remoting or RDP tracing
- **Add Linux-based endpoints** to test cross-platform detection coverage
- **Incorporate endpoint telemetry** from EDR tools like Velociraptor or KAPE
- **Extend awareness materials** into video or interactive modules

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.


