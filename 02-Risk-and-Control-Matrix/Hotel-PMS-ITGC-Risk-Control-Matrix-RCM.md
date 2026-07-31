# Risk & Control Matrix (RCM) — Hotel Property Management System ITGCs

**Scope:** Grand Horizon Hotels & Resorts — PMS Core Infrastructure  

---

| Control ID | COBIT 2019 Ref | Risk Description | Control Activity / Requirement | Control Type | Frequency | Test Procedure |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ITGC-AC-01** | DSS05.04 | Unauthorized access granted to PMS, exposing guest PII and billing records. | All new user accounts require formal HR ticket request and supervisor approval prior to creation. | Preventive | Event-driven | Inspect sample of 25 new accounts for written approval tickets. |
| **ITGC-AC-02** | DSS05.04 | Terminated staff retain active logins, leading to fraudulent transaction postings. | User access must be revoked within 24 hours of employee departure (Leaver SLA). | Corrective | Daily / Event | Compare HR termination logs against active PMS/AD user list. |
| **ITGC-OPS-01** | DSS01.01 | Night Audit EOD financial batch job fails or drops transactions during posting. | Nightly EOD batch scripts run automatically; failures trigger automated alerts to IT Duty Engineer. | Automated | Daily | Inspect EOD batch execution logs for 30 consecutive days. |
| **ITGC-OPS-02** | APO13.01 | PMS database corruption occurs with no recovery option. | Full database backups execute nightly at 03:00 AM and replicate to offsite AWS cloud storage. | Corrective | Daily | Verify backup job completion logs and test AWS S3 bucket sync state. |
| **ITGC-OPS-03** | APO13.02 | Database backup tapes/files cannot be restored during a disaster. | Backup restoration drills are executed quarterly in a isolated sandbox environment. | Detective | Quarterly | Review quarterly restoration test report and verify checksum accuracy. |
| **ITGC-SEC-01** | DSS05.02 | Guest credit card data compromised via infected guest Wi-Fi connection. | Hardware firewalls isolate Payment POS network (VLAN 20) from Guest Wi-Fi (VLAN 30). | Preventive | Continuous | Inspect firewall routing rules and perform VLAN isolation ping test. |
