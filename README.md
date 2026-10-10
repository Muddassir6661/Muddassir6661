# Hey, I'm Mohammed Muddassir Fareed 

Final-year CSE student (graduating April 2027), working toward a career in cybersecurity. I'm starting with SOC analyst roles because I like the detective side of security: watching what's happening, figuring out what's real, and explaining why.
_(Though I do love me some loopholes and vulnerabilities, but that's for another day)_

I learn best by building things, breaking them on purpose, and writing down what went wrong.

## What I'm working on right now

- Growing my cybersecurity homelab: next up is command injection detection and bringing RedSim in as an attack source
- Working through TryHackMe's SOC Level 1 path
- Planning my final-year project: an adversary emulation framework mapped to MITRE ATT&CK (RedSim v2)
- Cisco Networking Essentials, on the side

## Projects

### [Cybersecurity Homelab (in progress)](https://github.com/Muddassir6661/cybersec-homelab)
An offense + defense lab on an old Celeron laptop with 4 GB of RAM. Debian 12, Docker, Portainer, DVWA as the target, and Wazuh as the SIEM.

What's working so far:
- Wazuh agent on the host, watching DVWA activity
- Custom detection rules for SQL injection, XSS, and SSH brute force (alerts after 5+ failed logins in 60 seconds)
- Ran a real SSH brute force with Hydra against a disposable test account and investigated the alerts
- Real-time file integrity monitoring on a copy of the DVWA web root
- Remote access to the lab over Tailscale
- Wazuh's vulnerability detection flagged CVE-2021-35331 on the host, which I'm patching

Still to do: command injection coverage, fixing IPv6, and pointing RedSim at the lab.
`Debian` `Docker` `Wazuh` `DVWA` `Hydra` `Tailscale`

### [RedSim](https://github.com/Muddassir6661/RedSim)
A network attack simulation toolkit for practicing and understanding common attack techniques in a controlled setup. Presented it solo at my college's internal hackathon and placed 3rd in my department. It's also the base for my final-year project.
`Python` `Scapy` `paramiko` `FastAPI`

### [AI-Based Intrusion Detection System](https://github.com/Muddassir6661/AI-Based-IDS)
A machine learning IDS trained on the CICIDS2017 dataset, comparing Random Forest and SVM for detecting malicious network traffic.
`Python` `scikit-learn` `Random Forest` `SVM`

### [SAT-SA: Supervisory Analytics Tool for SOC Assessment](https://github.com/Muddassir6661/sat-sa)
Built for Smart India Hackathon 2026 (NTRO, Blockchain & Cybersecurity theme), where I led a team of 5 (Team SOCrates). It's an offline tool that looks at alert metadata and flags gaps in how a SOC handled alerts, like missing evidence. Built and tested on a synthetic dataset.
`Python` `FastAPI` `React` `Isolation Forest`

### Smart India Hackathon 2025
Part of a team that built an internship portal.

## Education

B.E. in Computer Science and Engineering, CGPA 8.91 (graduating April 2027)

## Certifications and courses

- SOC Analyst Course, PSF Skills Academy (July 2026)
- Mastercard Cybersecurity Job Simulation, Forage (August 2026)
- Deloitte Australia Cyber Job Simulation, Forage (August 2026)
- TryHackMe Pre Security Learning Path (August 2026)
- Getting Started with Cisco Packet Tracer, Cisco Networking Academy (August 2026)

## Achievements

- 3rd rank in department, DCET Internal Hackathon 2026 (RedSim)
- Led Team SOCrates (5 members) at Smart India Hackathon 2026

## Tools and skills

**Security:** Wazuh (SIEM), custom detection rules, file integrity monitoring, Hydra, Scapy, DVWA, network analysis, intrusion detection
**Languages:** Python
**Systems:** Linux (Debian), Docker, Portainer, Tailscale, Cisco Packet Tracer
**ML and web:** scikit-learn, FastAPI, React

## Find me

[LinkedIn](https://linkedin.com/in/muddassirfareed)

_Currently looking for entry-level cybersecurity roles and internships._
