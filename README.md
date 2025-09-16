# 🛡️ Wazuh SIEM Home Lab – SOC-Ready Cybersecurity Project

**Author:** Turki Alajmi  
**Status:** ✅ Completed – *Testing Phase Continues*  
**Certifications:** CompTIA Security+ & More

**LinkedIn:** www.linkedin.com/in/turki1alajm1
---

## 📖 Overview
This project showcases a **Security Operations Center (SOC)–ready Wazuh SIEM home lab**, built from scratch using **Ubuntu virtual machines on VirtualBox**.  
It demonstrates how to **detect, analyze, and respond** to real-world cyber threats, including:

- 🚨 **SSH Brute-Force Attacks**  
- 🔍 **Nmap Port Scans**  
- ⚡ **Privilege Escalation Attempts**

> ⚡ **Important:** This lab is **strictly for educational and defensive cybersecurity purposes**.

<img width="1919" height="994" alt="image" src="https://github.com/user-attachments/assets/d24b595a-023d-4d7c-9d7d-df7ee90cccd3" />


---

## 🏗️ Architecture

| Layer | Component | Purpose |
|-------|-----------|---------|
| 🖥️ **Host Machine** | Windows 10/11 | Runs VirtualBox and manages all VMs |
| 🧩 **VirtualBox VM** | Hypervisor | Creates isolated Ubuntu servers |
| 🐧 **Ubuntu Server** | Wazuh Manager | SIEM server receiving logs & alerts |
| 🟣 **Ubuntu Agent** | Endpoint | Simulates real-world endpoints & threats |
| 🌐 **Network** | Host-only / NAT | Segregated lab network for controlled attacks |

<img width="1919" height="995" alt="image" src="https://github.com/user-attachments/assets/d681bbe9-200d-43d1-8d31-366db0373fb4" />



---

## 🛠️ Tools & Technologies

| Category | Tools |
|----------|-------|
| **Virtualization** | Oracle VirtualBox |
| **Operating System** | Ubuntu 24.04 LTS |
| **SIEM/XDR** | Wazuh v4.12 |
| **Security Testing** | Nmap, Hydra (SSH brute force) |
| **Documentation** | GitHub README, Screenshots |

---

## 🚀 Step-by-Step Setup

### 1️⃣ Prepare the Environment
- Install **VirtualBox** on your host machine.
- Download the **Ubuntu 24.04 LTS** ISO.
- Create **two VMs**:
  - `wazuh-manager`
  - `ubuntu-agent`

<img width="661" height="572" alt="image" src="https://github.com/user-attachments/assets/3ba7ead8-8476-4042-98e9-2c97f5e858a6" />


---

### 2️⃣ Install and Configure Wazuh Manager
- Deploy **Wazuh Manager** on the first VM.
- Configure the **Wazuh Dashboard** for remote access.

<img width="520" height="375" alt="image" src="https://github.com/user-attachments/assets/eb3acbed-c844-4352-af4b-5d2ad9aa4150" /> <img width="694" height="342" alt="image" src="https://github.com/user-attachments/assets/5bea145d-5985-4303-9d91-551c4d8aa324" />



---

### 3️⃣ Deploy and Connect Ubuntu Agent
- Install **Wazuh Agent** on the second VM.
- Link the agent to the Wazuh Manager using the Manager IP (e.g., `192.168.xx.xx`).
- ✅ Verify successful registration on the **Agents** tab.

<img width="672" height="333" alt="image" src="https://github.com/user-attachments/assets/599e097b-e9ee-4415-b2de-f5ba62b9b0c9" />


---

### 4️⃣ Enable Core Security Modules
- ✅ **File Integrity Monitoring (FIM)**  
- ✅ **Vulnerability Detection (CVE mapping)**  
- ✅ **Threat Hunting & MITRE ATT&CK**

> ⚡ **Tip:** Edit `/var/ossec/etc/ossec.conf` to enable `<vulnerability-detection>` and `<syscollector>` modules.

---

### 5️⃣ Simulate Attacks
Performed **controlled attack simulations** to trigger alerts:

| Attack | Tool | Goal |
|--------|------|------|
| 🚨 **SSH Brute Force** | Hydra | Test brute-force detection |
| 🔍 **Nmap Scan** | Nmap | Identify open ports and test port-scan alerts |
| ⚡ **Privilege Escalation** | Custom script | Simulate privilege abuse |

<img width="1919" height="993" alt="image" src="https://github.com/user-attachments/assets/ba5ac15a-4a56-40e6-9007-02b710bb8630" /> <img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/9380c4c7-5a74-4681-8ab1-d80183cd9801" /> <img width="1919" height="996" alt="image" src="https://github.com/user-attachments/assets/ae6acfee-01ae-40a5-ba6a-fc1dd6aa8a21" />




---

### 6️⃣ Analyze Vulnerabilities & Respond
- Used Wazuh **Vulnerability Detection** to identify **critical CVEs**, e.g.:
  - `CVE-2023-3326`
  - `CVE-2022-3219`
  - `CVE-2025-9187`
- Documented **remediation steps**:
  - 🩹 Apply security patches:  
    ```bash
    sudo apt update && sudo apt upgrade
    ```
  - 📦 Update affected packages (e.g., `sudo apt install --only-upgrade firefox`).
  - 🔐 Adjust configurations to reduce risk until patches are applied.


---

## ✅ Key Outcomes
- Built a **production-like SIEM** from scratch.  
- Detected and analyzed **critical CVEs**, mapped to **MITRE ATT&CK** techniques.  
- Practiced **full SOC workflow**: detection → analysis → remediation.

> 💡 **Highlight:** Demonstrates end-to-end **Blue Team / SOC Analyst capabilities**.

---

## 🧪 Learning & Next Phase
This lab is currently in a **testing phase**.  
I will continue enhancing detection and response capabilities by **learning from advanced SIEM practices**, including:

> 🎥 Following the tutorial: [YouTube – Free Cybersecurity Tool: Wazuh SIEM/XDR](https://www.youtube.com/watch?v=v_6VWB-_wtw)

Planned improvements:
- 🧩 Deeper rule tuning & alert correlation  
- 🔄 Integration with cloud workloads  
- 📈 Advanced dashboards & automated responses

<img width="1082" height="721" alt="image" src="https://github.com/user-attachments/assets/84db2d88-23c7-4dca-9de8-0703865b0148" />

---

## 📷 More Images 
<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/ad92f954-c6ec-40e5-b5a6-c39cd34e0e7b" />
<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/0bdd50d2-350d-457c-847b-0becbf4dd56b" />
<img width="1919" height="989" alt="image" src="https://github.com/user-attachments/assets/52c606d2-cc8c-4f80-9ba2-2986aa6b1822" />
<img width="1909" height="972" alt="image" src="https://github.com/user-attachments/assets/2e22fe2a-e016-4673-8cf8-62299ac7ba1c" />

---

## 🔁 How to Reproduce
Clone this repository:
```bash
git clone https://github.com/tk-alajmi/SIEM.git
