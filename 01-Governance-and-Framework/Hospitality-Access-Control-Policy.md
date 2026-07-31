# Standard Operating Procedure (SOP): Hospitality User Access Governance

**Policy Reference:** SOP-HOT-AC-002  
**Applies To:** All Front Desk Agents, Night Auditors, Duty Managers, and IT Administrators  
**Effective Date:** January 15, 2026  

---

## 1. Principle of Least Privilege & Role-Based Access (RBAC)
Access to the Property Management System (PMS) and Point of Sale (POS) systems must be granted strictly according to approved job functions.

* **Front Desk Agent:** Granted access to check-in/check-out guest routines, assign rooms, and accept payment methods. Restricted from adjusting posted room charges or modifying system audit logs.
* **Night Auditor:** Granted temporary elevated access during late-night shifts to run End-of-Day (EOD) financial posting batch jobs and execute cashier closing reconciliations.
* **Hotel General Manager / Controller:** Read-only access to financial reports and override authorization for refunds exceeding $250.
* **IT Administrator:** System configuration access only. Direct operational transaction entry into guest folios is prohibited.

---

## 2. Joiner-Mover-Leaver (JML) Process Lifecycle

```text
[HR Employee Event] ---> [IT Service Desk Ticket] ---> [System Provisioning / Deprovisioning]
   (Joiner/Leaver)          (Required within SLA)             (AD & PMS Directives)
```

### A. Joiners (New Hires)
1. HR submits a new user provisioning request ticket 48 hours prior to the start date.
2. IT Service Desk creates a unique Active Directory account (naming convention: `firstname.lastname@grandhorizon.com`).
3. Shared logins (e.g., `frontdesk1`, `reception_night`) are **strictly prohibited**.

### B. Movers (Role Changes / Promotions)
1. Role changes require a written request signed by the Department Manager.
2. Prior role permissions must be purged within 24 hours of starting the new position.

### C. Leavers (Terminations)
1. **Voluntary Termination:** HR notifies IT on or before the final working shift. Access revoked within **24 hours**.
2. **Involuntary / Immediate Termination:** HR notifies IT immediately. Access revoked within **1 hour** of notification.

---

## 3. Password & Authentication Standards
* **Minimum Length:** 14 characters for domain logins; 8-digit complex PINs for POS terminals.
* **Multi-Factor Authentication (MFA):** Mandatory for remote PMS cloud access and IT administrative accounts.
* **Session Auto-Lock:** Inactivity auto-lock set to 3 minutes on all front desk endpoints.
