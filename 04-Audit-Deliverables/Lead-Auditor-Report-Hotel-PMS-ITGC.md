# IT General Controls (ITGC) Audit Executive Report — Hotel PMS Operations

**To:** Audit Committee & VP of Information Technology, Grand Horizon Hotels & Resorts  
**From:** Lead IT Auditor  
**Scope:** Property Management System (PMS), Front Desk Access Governance, Night Audit EOD Batch  
**Standards:** COBIT 2019, PCI-DSS v4.0, NIST SP 800-53 Rev. 5  

---

## Executive Summary

An IT General Controls (ITGC) audit was performed on the enterprise Property Management System (PMS) and supporting IT infrastructure. The scope spanned front desk user provisioning, night audit financial end-of-day (EOD) processing, database backup routines, and payment terminal network segmentation.

Overall, the control environment is **Satisfactory**, with robust controls observed in payment network segmentation (PCI-DSS isolation) and automated night audit database backups.

---

## Audit Finding Summary

```text
+-------------------------------------------------------------+
|  Major Non-Conformities Identified: 0                       |
|  Minor Non-Conformities Identified: 1                       |
|  Opportunities for Improvement (OFI): 2                     |
+-------------------------------------------------------------+
```

### Minor Non-Conformity (NC-01): Delayed Access Revocation for Terminated Staff (Leaver JML)
* **Control Reference:** COBIT 2019 DSS05.04 / PCI-DSS v4.0 Req 8.2.6
* **Finding:** Testing of a sample of 25 departed hotel staff members revealed that 3 front-desk agents retained active VisualMatrix PMS login accounts for 5 to 12 days past their official termination date.
* **Root Cause:** Front office supervisors failed to submit HR termination notification tickets in a timely manner prior to shift handovers.
* **Corrective Action Request (CAR):** Implement automated single sign-on (SSO) integration between HR identity software and PMS user directories to trigger immediate account disabling upon HR status change.

### Opportunity for Improvement (OFI-01): Night Audit Backup Restoration Drills
* **Control Reference:** NIST SP 800-53 CP-10 (System Recovery)
* **Observation:** Automated nightly PMS database backups execute successfully, but quarterly restoration testing is documented manually in logbooks without automated checksum validation.
* **Recommendation:** Automate quarterly backup restoration testing in a sandbox environment with automated integrity check reports.

### Opportunity for Improvement (OFI-02): POS Terminal Physical Inspection Logs
* **Control Reference:** PCI-DSS v4.0 Req 9.9.2
* **Observation:** Front desk and bar payment terminals undergo periodic physical tamper checks, but inspection logs are recorded on physical paper checklists subject to loss.
* **Recommendation:** Transition paper checklists to a centralized digital audit logging system.

---

## Overall Assessment Statement

The enterprise hotel IT environment demonstrates effective controls over core financial processing and credit card network security. Upon execution of automated HR-to-PMS deprovisioning for NC-01, the ITGC posture will meet enterprise compliance targets.
