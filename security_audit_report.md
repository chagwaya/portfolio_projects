# **🔍 Security Audit Report: Botium Toys**

## **📌 Controls Assessment Checklist**

| ✅ Yes | ❌ No | **Control** | **Explanation** |
|------|------|-------------|---------------|
| ❌ | **Least Privilege** | Currently, all employees have access to customer data. Privileges need to be restricted to reduce the risk of a breach. |
| ❌ | **Disaster Recovery Plans** | No disaster recovery plans are in place. These need to be developed to ensure business continuity. |
| ❌ | **Password Policies** | Employee password requirements are minimal, making it easier for threat actors to compromise systems. |
| ❌ | **Separation of Duties** | The CEO currently manages both daily operations and payroll. Implementing separation of duties can reduce fraud risks. |
| ✅ | **Firewall** | The existing firewall blocks traffic based on predefined security rules. |
| ❌ | **Intrusion Detection System (IDS)** | The IT department lacks an IDS, making it harder to detect intrusions. |
| ❌ | **Backups** | Critical data backups are missing, increasing the risk of data loss in case of a breach. |
| ✅ | **Antivirus Software** | Antivirus software is installed and regularly monitored. |
| ❌ | **Legacy System Monitoring** | Legacy systems are monitored, but there is no formal schedule or intervention policies in place. |
| ❌ | **Encryption** | Sensitive data is not encrypted, putting confidentiality at risk. |
| ❌ | **Password Management System** | No password management system exists, increasing the likelihood of password-related security breaches. |
| ✅ | **Physical Security (Locks, CCTV, Fire Detection)** | Adequate physical security measures, including locks, CCTV, and fire detection, are in place. |

---

## **📑 Compliance Checklist**

### **Payment Card Industry Data Security Standard (PCI DSS)**
| ✅ Yes | ❌ No | **Best Practice** | **Explanation** |
|------|------|----------------|---------------|
| ❌ | **Restrict Credit Card Data Access** | All employees have access to credit card data; only authorized personnel should have access. |
| ❌ | **Secure Processing & Storage** | Credit card data is neither encrypted nor stored securely. |
| ❌ | **Encryption for Transactions** | No encryption is used for credit card transactions, increasing the risk of data breaches. |
| ❌ | **Strong Password Policies** | Weak password policies increase the risk of unauthorized access. |

### **General Data Protection Regulation (GDPR)**
| ✅ Yes | ❌ No | **Best Practice** | **Explanation** |
|------|------|----------------|---------------|
| ❌ | **Protect E.U. Customer Data** | Encryption is not in place to ensure the security of personal data. |
| ✅ | **Breach Notification Plan** | A process exists to notify E.U. customers of a data breach within 72 hours. |
| ❌ | **Classify & Inventory Data** | Data assets have been inventoried but not classified. |
| ✅ | **Enforce Privacy Policies** | Privacy policies and procedures are in place and enforced among employees. |

### **System and Organization Controls (SOC 1 & SOC 2)**
| ✅ Yes | ❌ No | **Best Practice** | **Explanation** |
|------|------|----------------|---------------|
| ❌ | **User Access Policies** | Least privilege and separation of duties have not been implemented, allowing employees unrestricted data access. |
| ❌ | **Sensitive Data Protection (PII/SPII)** | Encryption is not used to ensure confidentiality of sensitive personal data. |
| ✅ | **Data Integrity** | Measures are in place to ensure data consistency, completeness, and accuracy. |
| ❌ | **Access Control Enforcement** | While data is accessible to employees, access should be restricted based on job roles. |

---

## **📢 Recommendations**

To strengthen security and compliance, **Botium Toys** should implement the following key measures:

### 🔹 **Security Controls**
- **Implement Least Privilege** – Restrict employee access to sensitive data based on role necessity.
- **Deploy an Intrusion Detection System (IDS)** – Enhance monitoring and threat detection capabilities.
- **Enforce Strong Password Policies** – Require complex passwords and enable multi-factor authentication (MFA).
- **Encrypt Sensitive Data** – Apply encryption to customer and financial data to improve confidentiality.
- **Establish a Disaster Recovery Plan** – Implement a structured plan to ensure business continuity in case of cyber incidents.
- **Schedule Regular Legacy System Maintenance** – Define a formal maintenance and intervention process for legacy systems.
- **Adopt a Password Management System** – Improve password security and reduce the risk of credential leaks.

### 🔹 **Compliance Enhancements**
- **Restrict Access to Credit Card Data** – Ensure only authorized personnel can handle payment information.
- **Classify Data Assets** – Implement a proper classification system to manage security controls effectively.
- **Enhance GDPR Compliance** – Apply encryption and strict access policies to protect E.U. customer data.
- **Regularly Review Security Policies** – Update policies to align with evolving security threats and compliance requirements.

By implementing these recommendations, **Botium Toys** can **reduce security risks, protect customer data, and enhance overall compliance with industry standards**. 🚀

