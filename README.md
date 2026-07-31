# Hotel Property Management System (PMS) Enterprise ITGC Audit Package

![Domain](https://img.shields.io/badge/Domain-Hospitality%20%26%20Hotel%20IT-blue)
![Framework](https://img.shields.io/badge/Framework-COBIT%202019%20%7C%20PCI--DSS%20v4.0%20%7C%20NIST%20CSF-red)
![Scope](https://img.shields.io/badge/Scope-Multi--Property%20PMS%20%26%20POS-gold)

## Executive Summary & Overview

This repository contains a comprehensive **IT General Controls (ITGC) Audit Framework** designed specifically for enterprise hotel operations and Property Management Systems (PMS, e.g., VisualMatrix PMS).

The simulated audit evaluates **Grand Horizon Hotels & Resorts**, assessing critical administrative, operational, and technical controls across front desk operations, night audit financial settlement workflows, and payment gateway infrastructure.

Hospitality IT environments present unique access control and operational continuity challenges:
1. **High Front-Desk Staff Turnover:** Managing high-volume Joiner-Mover-Leaver (JML) lifecycles to prevent orphaned user accounts and privilege creep across front desk agents and night auditors.
2. **Night Audit EOD Batch Integrity:** Safeguarding end-of-day (EOD) financial batch processing, room-rate postings, and automated database backups executed during late-night shifts.
3. **Cardholder Data Isolation (PCI-DSS v4.0):** Ensuring point-of-sale (POS) card reader terminals and PMS guest billing profiles strictly segregate credit card data from general hotel administrative networks.

---

## 📁 Repository Structure

```text
Hotel-PMS-Enterprise-ITGC-Audit-Package/
├── README.md
├── 01-Governance-and-Framework/
│   ├── ITGC-Audit-Charter-and-Scoping.md
│   └── Hospitality-Access-Control-Policy.md
├── 02-Risk-and-Control-Matrix/
│   └── Hotel-PMS-ITGC-Risk-Control-Matrix-RCM.md
├── 03-Audit-Workpapers/
│   ├── JML-Access-Control-Testing-Workpaper.md
│   └── Night-Audit-Backup-Batch-Testing-Workpaper.md
└── 04-Audit-Deliverables/
    └── Lead-Auditor-Report-Hotel-PMS-ITGC.md
```

---

## 🎯 Key Compliance & Security Controls Tested

```text
+-----------------------------------------------------------------------------------+
|                           Hotel Core IT Network Gateway                           |
|      [Property Management System (PMS)] <---> [Central Reservations Engine]       |
+-----------------------------------------------------------------------------------+
                                          |
                                 [Enterprise Firewall]
                                          |
        +---------------------------------+---------------------------------+
        |                                 |                                 |
 [VLAN 10: Front Desk & PMS]  [VLAN 20: Payment POS]         [VLAN 30: Guest Wi-Fi]
 (Staff JML & Night Audit)    (PCI-DSS Isolated Network)   (Isolated Public Access)
```

* **Joiner-Mover-Leaver (JML) Access Governance:** Auditing front-desk and night audit user provisionings/deprovisionings to verify timely revocation upon employee departure.
* **Night Audit Batch & Backup Integrity:** Testing automated nightly database snapshots, transaction posting logs, and off-site backup vaulting routines.
* **Payment Network Isolation (PCI-DSS v4.0):** Verifying 802.1Q VLAN separation and point-to-point encryption (P2PE) between card payment terminals and the hotel administrative core.

---

## 🛠️ Audit Standards & Reference Frameworks

* **COBIT 2019** — Domain DSS05 (Managed Security Services) & APO13 (Managed Security)
* **PCI-DSS v4.0** — Payment Card Industry Data Security Standard (Requirements 7, 8, and 10)
* **NIST SP 800-53 Rev. 5** — Security and Privacy Controls for Information Systems (AC & CP Families)

---

## ⚠️ Disclaimer

*All company names, hotel property names, employee identifiers, logs, and audit data contained within this repository are synthetic and created strictly for portfolio demonstration purposes.*
