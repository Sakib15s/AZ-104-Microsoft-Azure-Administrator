# Lab 01 – Creating a User Account and Assigning Licenses & Administrator Roles

### Objective
Create a new user in Microsoft Entra ID (Azure AD), assign a Microsoft Intune license, and grant the Intune Administrator role.

---

### Steps Performed

#### 1. Create a New User
- Navigated to **Microsoft Entra ID** > **Users** > **+ New user**.  
- Selected **Create user**.
- Entered:
  - **Username:** `User1`
  - **Name:** `User1`
  - (Other properties will be configured later as needed.)
- Skipped group or role assignment for now.
- Reviewed and created the user account successfully.

**Result:** A new user named **User1** was created.

---

#### 2. Assign License to the User
- Navigated to **Microsoft Entra ID** > **Users** > **User1** > **Licenses**.  
- Initially, no licenses were found for the user.
- Opened the **Microsoft 365 Admin Center**.
- Assigned the **Microsoft Intune Suite** license to **User1**.

**Result:** User1 now has an active Intune license.

---

#### 3. Assign Intune Administrator Role
- In **Microsoft Entra ID**, selected **User1** > **Assigned roles**.
- Clicked **Add assignments**.
- Selected **Intune Administrator** and confirmed the assignment.

**Result:** User1 has been granted the **Intune Administrator** directory role.

---

### Verification
- Confirmed **User1** is listed under **Users** with the correct license.
- Verified the **Intune Administrator** role assignment under directory roles.

---

### What I Learned
- How to create a new user in Microsoft Entra ID.
- How to assign Microsoft Intune licenses via the Microsoft 365 Admin Center.
- How to delegate administrative privileges using directory roles.
- The relationship between user accounts, licenses, and role-based access control (RBAC) in Microsoft Intune.

---

### Tools Used
- Microsoft Entra Admin Center  
- Microsoft 365 Admin Center  

---

### Next Steps
- Configure additional user properties.  
- Assign the user to Intune groups for policy and app deployment testing.

---

**Date Completed:** *(add your date here)*  
**Author:** *(your name or GitHub handle)*
