
# **🔍 Incident Report Analysis - NIST Cybersecurity Framework**  
**Company:** ORATECH MULTIMEDIA COMPANY  
**Incident Type:** **DDoS Attack (ICMP Flooding)**  
**Date:** 3/26/2025 
**Analyst: Newton Idala 

---

## **🛑 1️⃣ Summary of the Incident**  
The company experienced a **Distributed Denial-of-Service (DDoS) attack**, where all **network services** suddenly stopped responding. A **flood of ICMP packets** overwhelmed the system, disrupting operations.  

The **cybersecurity team** identified the attack, implemented mitigation measures, and restored critical network services.  

---

## **🔎 2️⃣ NIST Cybersecurity Framework (CSF) Analysis**  

The following table outlines how the **NIST CSF** was applied to this incident:  

| **NIST Function**  | **Action Taken**  | **Key Security Measures** |
|------------------|----------------|---------------------|
| **🔹 Identify** | Recognized an ongoing DDoS attack targeting the internal network. | Determined affected resources and prioritized securing critical network assets. |
| **🛡️ Protect** | Implemented a firewall rule to limit ICMP packet flooding. | **Firewall rules updated, IDS/IPS deployed, rate limiting enforced.** |
| **🕵️ Detect** | Monitored abnormal network traffic and identified attack sources. | **Enabled IP verification, deployed network monitoring tools.** |
| **🚨 Respond** | Isolated affected systems and stopped non-critical services. | **Analyzed network logs, reported findings, and informed management.** |
| **🔄 Recover** | Restored critical systems and blocked future ICMP flood attacks. | **Reinforced firewall protections, updated security policies.** |

---

## **📌 3️⃣ Detailed Incident Response**  

### **🛑 Identify**  
- The **DDoS attack** targeted the company's **internal network**, affecting all services.  
- The **cybersecurity team** confirmed a **high volume of ICMP packets** from multiple sources.  
- Affected resources were **logged and prioritized for restoration**.  

### **🛡️ Protect**  
- Implemented a **new firewall rule** to **limit ICMP packet rates**.  
- **Deployed IDS/IPS** to detect and filter out suspicious ICMP traffic.  
- Disabled **unnecessary ICMP responses** to reduce attack surface.  

### **🕵️ Detect**  
- Configured **source IP verification** to detect **spoofed addresses**.  
- Used **network monitoring tools** (e.g., Wireshark, Snort) to analyze attack traffic.  
- Identified unusual **traffic patterns and attack origins**.  

### **🚨 Respond**  
- **Isolated compromised systems** to prevent further network impact.  
- **Stopped non-critical services** to free up resources for critical functions.  
- **Reported incident findings** to **upper management & legal authorities** (if required).  
- Conducted a **forensic analysis** of attack logs for intelligence gathering.  

### **🔄 Recover**  
- **Restored critical services** in a **phased approach** (e.g., DNS, database, application servers).  
- Configured **firewalls to block external ICMP flood attacks**.  
- Developed **a response playbook** for future **DDoS mitigation strategies**.  
- Recommended **continuous network traffic monitoring** to detect similar threats early.  

---

## **✅ 4️⃣ Key Security Recommendations**  

To strengthen defenses against future **DDoS attacks**, the following **security measures** should be implemented:  

1. **Enhance Firewall Rules** → Restrict ICMP traffic and apply **rate limiting** on network devices.  
2. **Deploy Intrusion Detection/Prevention Systems (IDS/IPS)** → Monitor **anomalous network activity**.  
3. **Implement Load Balancers & Content Delivery Networks (CDN)** → Reduce **DDoS impact**.  
4. **Improve Logging & Monitoring** → Use **SIEM tools** to analyze attack patterns.  
5. **Develop a DDoS Response Plan** → Establish **automated mitigation** and **failover mechanisms**.  

---

## **🔚 5️⃣ Conclusion**  

This incident highlights the **importance of proactive security measures** and **real-time monitoring** to defend against **DDoS attacks**. By implementing the recommended **security controls**, the company can **minimize disruptions, enhance incident response, and strengthen its cybersecurity posture**.  

> **Next Steps:** **Conduct security training, implement advanced threat detection tools, and perform regular penetration testing** to stay ahead of emerging threats.  

1️⃣ Flowchart: DDoS Attack & Response Process
Here’s a visual representation of how the attack occurred and the incident response steps:
graph TD;
    A[DDoS Attack Initiated] -->|ICMP Flood| B[Network Services Overloaded]
    B -->|Traffic Monitoring| C[Incident Detected]
    C -->|Firewall Rule Updated| D[ICMP Rate Limiting]
    C -->|IDS Configured| E[Threat Actor Identification]
    D -->|Traffic Normalized| F[System Recovery]
    E -->|Report Incident| G[Security Policy Updates]
    F -->|Implement Defense Strategies| H[Future Protection]
    G -->|Improve Incident Response Plan| H

To block excessive ICMP requests, you can apply a rate-limiting rule using iptables:
sudo iptables -A INPUT -p icmp --icmp-type echo-request -m limit --limit 1/s --limit-burst 5 -j ACCEPT
sudo iptables -A INPUT -p icmp --icmp-type echo-request -j DROP

📌 Explanation:
Allows only 1 ICMP request per second with a burst limit of 5.
Drops all additional ICMP packets beyond the threshold.

3️⃣ Sample Network Log (Wireshark Capture)
A sample log snippet showing ICMP flood attack attempts:
Time       Source IP      Destination IP     Protocol   Length  Info
12:45:01   192.168.1.5    10.0.0.1          ICMP       98      Echo Request
12:45:01   192.168.1.5    10.0.0.1          ICMP       98      Echo Request
12:45:01   192.168.1.5    10.0.0.1          ICMP       98      Echo Request
12:45:02   192.168.1.5    10.0.0.1          ICMP       98      Echo Request

📌 How to Use This in the Report:
Include sample attack logs to demonstrate threat detection.
Helps security teams analyze attack behavior.
