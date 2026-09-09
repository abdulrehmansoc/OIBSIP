# Task 4: Network Threat Analysis Report

## Executive Summary
Modern enterprise networks face an evolving array of cyber threats that target network infrastructure, data integrity, and system availability. This report provides a detailed security analysis of common network-level threats, attack vectors, detection mechanisms, and defensive mitigation strategies.

---

## 1. Common Network Threats & Attack Vectors

### 1.1 Man-in-the-Middle (MitM) Attacks
* **Overview:** An attacker secretly relays and alters communications between two parties who believe they are directly communicating.
* **Vectors:** ARP Spoofing, DNS Cache Poisoning, Rogue Wi-Fi Access Points.
* **Impact:** Interception of credentials, sensitive data leakage, and session hijacking.

### 1.2 Distributed Denial of Service (DDoS)
* **Overview:** Malicious actors overwhelm target servers or networks with high-volume traffic to disrupt service availability.
* **Vectors:** SYN Flooding, UDP Amplification, DNS Amplification, HTTP Flood.
* **Impact:** Service outage, financial loss, and operational disruption.

### 1.3 Unauthorized Reconnaissance & Scanning
* **Overview:** Adversaries probe network ports and services to identify exposed vulnerabilities before launching an attack.
* **Vectors:** Nmap SYN Scans, Sweep Scans, OS Fingerprinting.
* **Impact:** Identification of vulnerable services for targeted exploitation.

---

## 2. Threat Detection & Log Analysis

To identify active network threats, Security Operations Center (SOC) analysts monitor network logs, IDS/IPS alerts, and firewall events:

* **Snort / Suricata IDS Rules:** Monitor signature-based anomalies across network packets.
* **Flow Logs (NetFlow / IPFIX):** Analyze traffic volume spikes indicative of data exfiltration or DDoS attacks.
* **DNS Query Monitoring:** Detect suspicious beaconing behavior and domain generation algorithms (DGA).

---

## 3. Recommended Defensive Controls & Mitigation Strategy

| Security Layer | Recommended Control | Objective |
|---|---|---|
| **Perimeter Defense** | Next-Generation Firewalls (NGFW) & WAF | Block unauthorized inbound and outbound traffic. |
| **Network Segmentation** | VLANs & Micro-segmentation | Prevent lateral movement across internal network zones. |
| **Encryption** | TLS 1.3 / IPsec VPN | Protect data-in-transit against sniffing and MitM attacks. |
| **Identity & Access** | 802.1X Port Security & MFA | Restrict network port access to authenticated devices only. |

---

## Conclusion & Next Steps
Implementing defense-in-depth controls across network perimeters and internal segments significantly mitigates network threat exposure. Continuous security monitoring via SIEM and regular network audits remain critical for early detection.
