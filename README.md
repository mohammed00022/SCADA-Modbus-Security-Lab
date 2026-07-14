# SCADA & OT Security Sandbox: Modbus Emulation & Attack Analysis

An educational, hands-on cybersecurity lab simulating an Operational Technology (OT) environment. This project demonstrates how industrial protocols (specifically Modbus TCP) communicate, analyzes their inherent security vulnerabilities, and builds an Intrusion Detection System (IDS) to defend against potential cyber threats.

---

## 🛠️ Project Architecture & Lab Setup

The lab is built using a virtualized sandbox environment (VirtualBox) mapped to **The Purdue Model** standards:
*   **Attacker Node (Level 3/4):** Kali Linux (Armed with custom Python scripts and packet manipulation tools).
*   **Engineering Station & PLC Emulator (Level 1/2):** Windows VM running Modbus TCP simulators (ModbusPal / QModMaster).
*   **Network Capture & IDS (Level 2/3):** Wireshark for deep packet analysis and Snort for detection.

---

## 📅 Roadmap & Implementation Steps

### 🔹 Phase 1: Emulation & Baseline Capture (In Progress)
*   Set up Host-Only networking to isolate VMs.
*   Emulate PLCs and initiate regular Modbus register read/write cycles.
*   Capture baseline network traffic using Wireshark to map Out-of-Bound registers.

### 🔹 Phase 2: Vulnerability Analysis & Attack Emulation
*   Demonstrate Modbus protocol's lack of authentication and encryption.
*   Execute unauthorized command injection (writing malicious values to registers).
*   Perform Modbus Reconnaissance scanning using Nmap.

### 🔹 Phase 3: Defensive Engineering & IDS Rules
*   Analyze malicious PCAP files to identify attack signatures.
*   Write custom Snort/IDS rules to detect unauthorized Modbus write commands.
*   Document incident response steps for industrial operators.

---

## 🏆 Key Takeaways & Skills Demonstrated
*   **Industrial Protocols:** Modbus TCP mechanics, Coil/Register mapping.
*   **OT Security:** Understanding the AIC (Availability, Integrity, Confidentiality) Triad.
*   **Network Security:** Traffic analysis (PCAP), Wireshark filtering, and signature-based detection.
