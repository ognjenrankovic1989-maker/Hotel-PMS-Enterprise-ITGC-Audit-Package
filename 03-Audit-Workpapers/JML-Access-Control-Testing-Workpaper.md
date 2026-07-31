# Audit Workpaper: Joiner-Mover-Leaver Access Control Testing (WP-ITGC-101)

**Audit Scope:** Front Desk & Night Audit Personnel Access Review  
**Testing Period:** January 1, 2026 – June 30, 2026  
**Auditor:** Lead IT Auditor  

---

## 1. Test Objective
To evaluate the operating effectiveness of user access provisioning and deprovisioning controls (ITGC-AC-01 & ITGC-AC-02) for employees accessing the VisualMatrix Property Management System (PMS).

---

## 2. Sample Selection
A sample of **25 employees** was selected from HR records across three categories:
* 10 New Hires (Joiners)
* 5 Role Transfers (Movers)
* 10 Terminated Employees (Leavers)

---

## 3. Detailed Test Execution & Results

| Sample ID | Employee ID | Role / Dept | Event Type | Effective Date | Access Updated Date | SLA Target | Result | Exception Notes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **SMP-01** | EMP-7712 | Front Desk Agent | Joiner | 2026-02-10 | 2026-02-09 | Met | **PASS** | Ticket HR-9921 attached. |
| **SMP-02** | EMP-7740 | Night Auditor | Joiner | 2026-03-01 | 2026-02-28 | Met | **PASS** | Ticket HR-1012 attached. |
| **SMP-03** | EMP-8109 | F&B Supervisor | Mover | 2026-04-15 | 2026-04-15 | Met | **PASS** | Old POS admin permissions removed. |
| **SMP-04** | EMP-8821 | Front Desk Agent | Leaver | 2026-05-10 | 2026-05-22 | Exceeded | **FAIL** | Account remained active **12 days** post-termination. |
| **SMP-05** | EMP-9104 | Front Desk Agent | Leaver | 2026-05-18 | 2026-05-23 | Exceeded | **FAIL** | Account remained active **5 days** post-termination. |
| **SMP-06** | EMP-9111 | Night Auditor | Leaver | 2026-06-01 | 2026-06-09 | Exceeded | **FAIL** | Account remained active **8 days** post-termination. |

*(Note: 19 remaining sample items tested passed all control criteria).*

---

## 4. Audit Finding & Exception Summary
* **Total Tested:** 25
* **Passed:** 22
* **Failed:** 3 (All within Leaver Deprovisioning)

**Finding Details:** 3 out of 10 terminated front desk staff members retained active VisualMatrix PMS and Active Directory accounts after their official separation dates (ranging from 5 to 12 days delay). 

**Root Cause:** Department supervisors failed to submit HR termination forms prior to shift handovers, leaving accounts active until monthly manual reconciliation.

**Ref Reference:** Formally documented as **Minor Non-Conformity (NC-01)** in Lead Auditor Report.
