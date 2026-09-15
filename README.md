# servicenow-ticketing-system-itsm-home-lab
ServiceNow ITSM lab demonstrating platform access control, user role assignments, IT Support Staff group routing, end-to-end incident lifecycle management, Active Directory lockout resolution, and custom reporting analytics.

### 1. User Provisioning & Account Creation
Configured platform access by provisioning a new support technician account (`Aidan.McCann`) as a Help Desk Technician in the IT Department.

<img width="2497" height="1541" alt="image" src="https://github.com/user-attachments/assets/c2a8a37e-7299-482a-8b3a-f261cee40f19" />

* **User ID:** Aidan.McCann
* **Title:** Help Desk Technician
* **Department:** IT
* **Account Status:** Active

<img width="2497" height="1543" alt="image" src="https://github.com/user-attachments/assets/9935e78c-577f-4ed3-bd94-aeaaa24b62d6" />

* **Account Audited:** `Aidan.McCann` (Aidan McCann)
* **Assigned Groups:** `IT Support Staff`, `Conditional Script Writer`
* **Group Count:** 2 Active Group Memberships

<img width="2495" height="1539" alt="image" src="https://github.com/user-attachments/assets/628ed294-b3e7-4e12-97f1-1d8d595ccc12" />
<img width="2496" height="1541" alt="image" src="https://github.com/user-attachments/assets/8b88d206-af9f-45c8-a415-c80ff2fa7306" />

* **Inherited Roles Count:** 44 platform roles automatically assigned via group memberships
* **Key Role Inherited:** `itil` (Grants full IT Service Management incident creation, update, and resolution capabilities)
* **Inheritance Status:** `Inherited = true` (Confirms Role-Based Access Control / RBAC best practices)


### 2. User Directory Verification & Account Confirmation
Verified successful creation and active status of the newly provisioned technician account within the ServiceNow global User directory (`sys_user`).

<img width="2497" height="1541" alt="image" src="https://github.com/user-attachments/assets/12a09352-3a9e-4cd2-8185-649508f8e806" />

* **Table Verified:** User Directory (`sys_user`)
* **Provisioned Account:** `Aidan.McCann` (Aidan McCann)
* **Status:** Active (`true`)
* **System Notification:** "Primary email device created for Aidan McCann"


### 3. Custom Assignment Group Provisioning
Configured and created a dedicated support assignment group within ServiceNow to handle incoming helpdesk and infrastructure workload routing.

<img width="2495" height="1542" alt="image" src="https://github.com/user-attachments/assets/59ff31b8-5e65-43bd-81d3-4544025d9b52" />

* **Group Name:** IT Support Staff
* **Group Manager Assigned:** Andrew Jackson
* **Description:** IT Support staff for mannilabs.com
* **Functional Scope:** Serves as the primary operational group queue for incident intake, triage, and escalation routing.


### 4. Group Record Configuration & Role Auditing
Opened the active `IT Support Staff` group record to verify group metadata and inspect assigned platform roles (`sys_user_group`).

<img width="2496" height="1540" alt="image" src="https://github.com/user-attachments/assets/8c80c0f2-9cff-4e5f-bb5a-b1928ea4601a" />

* **Group Record:** `IT Support Staff`
* **Related List View:** `Group Members (1)` tab
* **Assigned Member:** Aidan McCann (`Aidan.McCann`)
* **Operational Result:** Provisioned technician account to receive and manage incidents assigned to the IT Support Staff group.


### 5. User Groups Directory Verification
Queried the ServiceNow User Groups directory (`sys_user_group`) using a custom name filter (`Name >= IT Support`) to verify active system support groups and confirm successful registration of the newly created team.

<img width="2495" height="1541" alt="image" src="https://github.com/user-attachments/assets/d7dcdd11-950b-4ed1-b070-f68e9943b60e" />

* **Table Accessed:** User Groups (`sys_user_group`)
* **Search Filter Applied:** `Name >= IT Support`
* **Filtered Results:** 25 matching groups displayed
* **Verified Group Record:** `IT Support Staff` (Manager: Andrew Jackson | Active: `true` | Description: `IT Support staff for mannilabs.com`)


### 6. Group Member Mapping (Slushbucket Configuration)
Utilized the ServiceNow slushbucket interface to assign technician account `Aidan McCann` from the global user directory to the `IT Support Staff` group queue.

<img width="2495" height="1546" alt="image" src="https://github.com/user-attachments/assets/b6e4bc8b-8173-4ab7-8578-31c21190d940" />

* **Interface:** Group Member - Edit Members (`sys_m2m_template`)
* **Target Group:** IT Support Staff
* **Selected Member:** Aidan McCann
* **Action:** Moved user record from the global Collection bucket into the active Group Members List to establish queue membership.


### 9. Incident Record Inspection & State Auditing
Opened incident record `INC0008111` to evaluate active ticket metadata, urgency categorization, and caller activity history within the Self-Service interface.

<img width="2496" height="1543" alt="image" src="https://github.com/user-attachments/assets/9a20115b-a18f-481a-87f0-bf2f57c2524d" />

* **Incident Number:** `INC0008111`
* **Caller:** System Administrator
* **State / Urgency:** `New` | `3 - Low`
* **Activity Stream:** Audited system-generated field changes, verifying initial priority calculation (`5 - Planning`) and logged timestamps.


### 10. Incident Directory Navigation & Queue Filtering
Navigated the ServiceNow Incident Directory (`incident`) using Self-Service queue filters to review active ticket workloads caller-specific query conditions.

<img width="2494" height="1544" alt="image" src="https://github.com/user-attachments/assets/92fa0b56-e83f-4a72-8d34-5fcf79a76085" />

* **Table Accessed:** Incident (`incident`)
* **View Mode:** Self Service
* **Query Filter Applied:** `Caller = System Administrator > Active = true > Universal Request is empty`
* **Operational Scope:** Verifies existing caller ticket history prior to logging new ITSM incidents.

