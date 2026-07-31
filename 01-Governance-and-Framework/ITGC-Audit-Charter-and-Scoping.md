# ITGC Audit Charter & Engagement Scoping Document

**Entity:** Grand Horizon Hotels & Resorts (Multi-Property Enterprise)  
**Audit Period:** Q1 - Q2 2026  
**Lead Auditor:** IT Internal Audit / GRC Team  
**Standards:** COBIT 2019, NIST SP 800-53 Rev. 5, PCI-DSS v4.0  

---

## 1. Audit Objective & Mandate
The objective of this IT General Controls (ITGC) audit is to evaluate the design and operating effectiveness of administrative, logical access, program change, and IT operational controls supporting core hospitality systems.

The scope focuses on key hotel management technologies directly impacting financial reporting, guest personal data, and credit card security.

---

## 2. In-Scope Systems & Assets

| Asset / System Name | Function / Description | Criticality | Target Compliance Standards |
| :--- | :--- | :--- | :--- |
| **VisualMatrix PMS** | Core Property Management System (Reservations, Guest Folios, Room Inventories) | **Critical** | COBIT 2019, PCI-DSS v4.0, GDPR |
| **Micros Simphony POS** | Food & Beverage Point of Sale system at outlets and bars | **High** | PCI-DSS v4.0 |
| **Active Directory (AD)** | Enterprise Identity & Access Management (Front Desk logins, Staff Domain Accounts) | **Critical** | NIST SP 800-53 AC-2 |
| **Veeam / AWS Backup** | Automated Nightly Database Backup & Cloud Archival Engine | **High** | NIST SP 800-53 CP-9 |
| **VingCard / Visionline** | Electronic Guest Cabin & Room Lock Management Server | **Medium** | COBIT 2019 DSS05.04 |

---

## 3. Out-of-Scope Items
* Guest Public Wi-Fi captive portals (evaluated under separate external vulnerability assessment).
* Third-party online travel agency (OTA) external interfaces (covered under vendor SOC 2 reports).

---

## 4. Key ITGC Control Domains Evaluated
1. **Logical Access & Identity Governance:** User onboarding, transfer role changes, and termination deprovisioning (JML).
2. **Night Audit Operations & End-of-Day (EOD) Processing:** Scheduled batch job executions, rate postings, and transaction log integrity.
3. **Data Backup & Business Continuity:** Automated database backup schedules, offsite replication, and restoration drill logs.
4. **Network & Infrastructure Security:** VLAN isolation separating payment card networks from general hotel administrative networks.
