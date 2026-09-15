# servicenow-ticketing-system-itsm-home-lab
ServiceNow ITSM lab demonstrating platform access control, user role assignments, IT Support Staff group routing, end-to-end incident lifecycle management, Active Directory lockout resolution, and custom reporting analytics.

### 1. User Provisioning & Account Creation
Configured platform access by provisioning a new support technician account (`Aidan.McCann`) as a Help Desk Technician in the IT Department.

<img width="2497" height="1541" alt="image" src="https://github.com/user-attachments/assets/c2a8a37e-7299-482a-8b3a-f261cee40f19" />

* **User ID:** Aidan.McCann
* **Title:** Help Desk Technician
* **Department:** IT
* **Account Status:** Active


### 2. User Directory Verification & Account Confirmation
Verified successful creation and active status of the newly provisioned technician account within the ServiceNow global User directory (`sys_user`).

<img width="624" height="386" alt="Picture2" src="https://github.com/user-attachments/assets/f270e59f-5d8a-4096-8e95-e1fe0e3dd831" />

* **Table Verified:** User Directory (`sys_user`)
* **Provisioned Account:** `Aidan.McCann` (Aidan McCann)
* **Status:** Active (`true`)
* **System Notification:** "Primary email device created for Aidan McCann"
