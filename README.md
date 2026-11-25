# kali-wsl-cybersec-labs

Kali Linux on WSL for authorized lab practice: Nmap, Wireshark, OWASP ZAP, Burp Suite, DVWA, and Metasploit in an isolated lab. All labs are on systems I own or lab VMs provided for training. No unauthorized access.

## Folder layout

| Folder | Focus |
| :--- | :--- |
| `01-network-lab/` | Host discovery, port scanning, and packet analysis (Nmap, Wireshark) |
| `02-web-app-lab/` | Web app testing against intentionally vulnerable targets (DVWA, OWASP Top 10, ZAP, Burp Suite) |
| `03-defense-lab/` | Perimeter and detection controls (firewall, ModSecurity WAF, Security Onion / SIEM) |
| `04-ai-security-evaluation/` | Evaluating AI / LLM outputs for security, accuracy, and safe code |

Metasploit is used for exploitation practice against lab targets only, inside the web-app and defense labs.

## Ground rules

- Only scan or test targets you own or are explicitly authorized to test.
- Keep lab targets on an isolated network, such as a host-only or internal virtual switch. Do not point tools at school, work, or public networks.
- Snapshot your VMs before running anything destructive.
- Keep a log of what you ran and when. It helps when you write up findings.

## Suggested setup order

1. Install Kali on WSL and update packages.
2. Build the targets: DVWA (or similar) in Docker or a VM, and a Security Onion instance if you want the defense lab.
3. Work through the folders in order: network, then web app, then defense, then AI security evaluation.