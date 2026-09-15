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

<img width="2497" height="1541" alt="image" src="https://github.com/user-attachments/assets/12a09352-3a9e-4cd2-8185-649508f8e806" />

* **Table Verified:** User Directory (`sys_user`)
* **Provisioned Account:** `Aidan.McCann` (Aidan McCann)
* **Status:** Active (`true`)
* **System Notification:** "Primary email device created for Aidan McCann"


### 3. User Groups Directory Verification
Queried the ServiceNow User Groups directory (`sys_user_group`) using a custom name filter (`Name >= IT Support`) to verify active system support groups and confirm successful registration of the newly created team.

<img width="1024" height="634" alt="image" src="https://github.com/user-attachments/assets/d42d5344-cabf-4183-aff3-6d84868db5ef" />

* **Table Accessed:** User Groups (`sys_user_group`)
* **Search Filter Applied:** `Name >= IT Support`
* **Filtered Results:** 25 matching groups displayed
* **Verified Group Record:** `IT Support Staff` (Manager: Andrew Jackson | Active: `true` | Description: `IT Support staff for mannilabs.com`)
