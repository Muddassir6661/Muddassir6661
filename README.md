# Hey, I'm Mohammed Muddassir Fareed

Final-year CSE student (graduating April 2027), working toward a career in cybersecurity. I'm starting with SOC analyst roles because I like the detective side of security: watching what's happening, figuring out what's real, and explaining why. *(Though I do love me some loopholes and vulnerabilities — but that's for another day)*

I learn best by building things, breaking them on purpose, and writing down what went wrong.

---

## What I'm working on right now

- **MyTRE** — my final-year major project, a full ATT&CK-mapped adversary emulation framework (16 technique modules, real campaign runs, blue team detection coverage)
- Growing and hardening my cybersecurity homelab (Wazuh SIEM + DVWA target)
- Working through TryHackMe's SOC Level 1 path
- Cisco Networking Essentials, on the side

---

## Projects

### [MyTRE — ATT&CK-Mapped Adversary Emulation Framework](https://github.com/Muddassir6661/mytre)

My final-year major project. MyTRE (a pun on MITRE) is a Python adversary emulation framework that chains 16 MITRE ATT&CK technique modules into a structured campaign, passes shared state across stages via a Context object (credentials found in stage 6 are automatically used in stage 12), and generates a pentest-style findings report in Markdown and HTML.

**16 modules across 7 ATT&CK tactics:**

| Tactic | Techniques |
|---|---|
| Reconnaissance | Port Scan (T1046), Service Fingerprint (T1592), Vuln Scan (T1595.002) |
| Initial Access | HTTP Default Creds (T1078), Command Injection (T1190) |
| Credential Access | SSH Brute Force (T1110.001), Credentials in Files (T1552) |
| Discovery | Account (T1087), Process (T1057), Network Config (T1016), File/Dir (T1083) |
| Lateral Movement | SSH Pivot (T1021.004), Lateral Tool Transfer (T1570) |
| Persistence | SSH Authorized Key (T1098) |
| Exfiltration | Local File Stage (T1074.001), HTTP Exfil (T1041) |

**Validated campaign results (real run, not simulated):**
- Full 16-stage campaign against personal homelab: **15/16 succeeded in 61.54 seconds**
- Only failure: VulnScan — expected, host is patched, no CVE match

**Wazuh (blue team) detections confirmed live:**
- Rule 100019 (level 12) — Brute force success detected
- Rule 100013 (level 10) — SSH brute force pattern detected
- Rule 100017 (level 10) — SSH authorized_keys write detected (T1098 persistence)
- Rule 100014 (level 7) — Command injection caught in real time
- Rule 100018 (level 8) — File dropped in /tmp detected (T1570 tool transfer)
- Rule 100016 (level 5) — HTTP exfil to receiver confirmed
- Email alerts configured and working

**Key design features:** YAML-driven campaigns with variable resolution · passwords never appear in reports or logs · selective stage execution · coloured live terminal UI · explicit confirmation before any campaign runs

`Python` `Paramiko` `Requests` `PyYAML` `DVWA` `Wazuh` `MITRE ATT&CK`

> *"RedSim taught me attacks in isolation. MyTRE taught me attacks as a structured campaign a real adversary would run — and then I built the detection side in Wazuh to see exactly what a defender sees when it happens."*

---

### [Cybersecurity Homelab](https://github.com/Muddassir6661/cybersec-homelab)

An offense + defense lab on an old Celeron laptop with 4 GB RAM. Debian 12, Docker, Portainer, DVWA as the target, and Wazuh as the SIEM. Now serving as the live target environment for MyTRE campaigns.

- Custom Wazuh detection rules covering command injection, SSH brute force, persistence, lateral movement, and HTTP exfiltration
- Real-time file integrity monitoring on the DVWA web root
- Remote access over Tailscale
- Email alerting configured and verified against real attack runs

`Debian` `Docker` `Wazuh` `DVWA` `Tailscale`

---

### [RedSim](https://github.com/Muddassir6661/RedSim)

A network attack simulation toolkit for practicing and understanding common attack techniques in a controlled setup. Placed 3rd in my college's internal hackathon. Served as the conceptual predecessor to MyTRE — RedSim runs techniques in isolation; MyTRE chains them into a full adversary campaign.

`Python` `Scapy` `Paramiko` `FastAPI`

---

### [AI-Based Intrusion Detection System](https://github.com/Muddassir6661/AI-Based-IDS)

A machine learning IDS trained on the CICIDS2017 dataset, comparing Random Forest and SVM for detecting malicious network traffic.

`Python` `scikit-learn` `Random Forest` `SVM`

---

### [SAT-SA: Supervisory Analytics Tool for SOC Assessment](https://github.com/Muddassir6661/sat-sa)

Built for Smart India Hackathon 2026 (NTRO, Blockchain & Cybersecurity theme), where I led a team of 5 (Team SOCrates). An offline tool that analyses alert metadata and flags gaps in how a SOC handled alerts — missing evidence, missed escalations. Built and tested on a synthetic dataset.

`Python` `FastAPI` `React` `Isolation Forest`

---

## Education

B.E. in Computer Science and Engineering, CGPA 8.91 (graduating April 2027)

---

## Certifications and courses

- SOC Analyst Course, PSF Skills Academy (July 2026)
- Mastercard Cybersecurity Job Simulation, Forage (August 2026)
- Deloitte Australia Cyber Job Simulation, Forage (August 2026)
- TryHackMe Pre Security Learning Path (August 2026)
- Getting Started with Cisco Packet Tracer, Cisco Networking Academy (August 2026)

---

## Achievements

- Final-year major project: MyTRE — ATT&CK-mapped adversary emulation framework with live Wazuh detection validation
- 3rd rank in department, DCET Internal Hackathon 2026 (RedSim)
- Led Team SOCrates (5 members) at Smart India Hackathon 2026

---

## Tools and skills

**Security:** MITRE ATT&CK, Wazuh (SIEM), custom detection rules, adversary emulation, file integrity monitoring, Hydra, Scapy, DVWA, network analysis, intrusion detection  
**Languages:** Python  
**Systems:** Linux (Debian), Docker, Portainer, Tailscale, Cisco Packet Tracer  
**ML and web:** scikit-learn, FastAPI, React

---

## Find me

[LinkedIn](https://linkedin.com/in/muddassirfareed)

*Currently looking for entry-level cybersecurity roles and internships.*
