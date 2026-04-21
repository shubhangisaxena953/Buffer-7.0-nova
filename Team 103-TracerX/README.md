# TracerX 🛡️
### Network Attack Path Analyzer

TracerX is an interactive network security visualization tool that maps and analyzes potential attack paths across your infrastructure. It uses the **CVSS 3.1** scoring system and aligns with the **MITRE ATT&CK Framework** to help security teams identify and prioritize vulnerabilities before attackers can exploit them.

---

## 🎥 Video

> A short walkthrough of TracerX showing live attack path analysis, node inspection, and vulnerability mapping.

** link **

---

## Features

- **Interactive Network Graph** — Visualizes all nodes in your network topology with real-time animated attack path overlays
- **Attack Path Ranking** — Automatically ranks attack paths by CVSS score, from Critical to Medium severity
- **Node Inspection** — Click any node to view its OS, open ports, risk score, and known CVEs
- **Dual View Modes** — Switch between Attack Path view and full Topology view
- **CVSS 3.1 Scoring** — Each attack path is scored using the industry-standard Common Vulnerability Scoring System
- **MITRE ATT&CK Alignment** — Vulnerability mapping follows the MITRE ATT&CK framework
- **Scan Simulation** — Trigger a new scan to refresh threat detection

---

## Tech Stack

- **Frontend:** Pure HTML, CSS, JavaScript (no frameworks)
- **Rendering:** HTML5 Canvas API for network graph and animations
- **Fonts:** JetBrains Mono, Sora (Google Fonts)
- **Styling:** CSS Variables for dynamic theming

---

## How It Works

1. The tool models your network as a graph of **nodes** (servers, firewalls, databases, etc.) and **edges** (connections between them)
2. It computes all possible **attack paths** from the internet to critical assets
3. Each path is scored using **CVSS 3.1** and mapped to real-world CVEs
4. The **Canvas renderer** animates the active attack path with moving threat indicators
5. Users can click nodes to inspect vulnerabilities and select different attack paths from the sidebar

---

## Sample Attack Paths Detected

| Path ID | CVSS | Route | Exploit Chain |
|---------|------|-------|---------------|
| AP-001 | 9.8 | Internet → Firewall → LB → Web1 → App → LDAP → DB | Log4Shell → AD PrivEsc → DB Admin |
| AP-002 | 9.1 | Internet → Firewall → LB → Web1 → App → DB | Path Traversal → Spring4Shell → DB |
| AP-003 | 8.8 | Internet → Firewall → LB → Web2 → App → API → DB | Sudo Exploit → RCE → DB Breach |
| AP-005 | 8.1 | Internet → Firewall → CI/CD → App → LDAP → DB | Jenkins RCE → AD Spoof → DB |

---

## CVEs Covered

- `CVE-2021-44228` — Log4Shell Remote Code Execution (CVSS 10.0)
- `CVE-2022-22965` — Spring4Shell RCE (CVSS 9.8)
- `CVE-2021-41773` — Apache Path Traversal (CVSS 9.8)
- `CVE-2019-9193`  — PostgreSQL Arbitrary Code Execution
- `CVE-2021-42278` / `CVE-2021-42287` — Active Directory Privilege Escalation
- `CVE-2021-40346` — HAProxy Integer Overflow (CVSS 8.6)
- `CVE-2021-3156`  — Sudo Heap Overflow (CVSS 7.8)
- `CVE-2021-21985` — Jenkins RCE via Script Console

---

## Team Nova

|         Name         |
|----------------------|
|  Shubhangi Saxena    |
|    Aarya Karekar     |
|   Shrayati Sharma    |
|   Hemakshi Parsai    |

---

## License

This project was built for educational and hackathon purposes.
