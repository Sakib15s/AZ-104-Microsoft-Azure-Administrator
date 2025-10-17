# Lab 02 – Creating and Managing Groups in Microsoft Intune

### Objective
Create and manage a security group in Microsoft Intune (via the Microsoft Entra admin center) to efficiently target licensed users for policies, configurations, and app deployments.

---

### Purpose of Groups
Groups in Intune simplify management by allowing administrators to:
- Assign apps, policies, or configurations to a collection of users or devices.
- Control access and permissions in a structured way.
- Ensure only licensed or relevant users receive specific Intune configurations.

In this lab, the goal is to **create a security group** that includes all users with Intune licenses — making it easier to apply settings consistently.

---

### Steps Performed

#### 1. Open Intune Admin Center
- Navigated to **Microsoft Intune Admin Center** > **Groups**.

#### 2. Create a New Group
- Clicked **+ New group**.

#### 3. Configure Group Information
- **Group type:** Security  
- **Group name:** `Intune Licensed Users`  
- **Description:** Group to manage all users with assigned Microsoft Intune licenses.  
- **Membership type:** Selected **Assigned** (will explore **Dynamic User** and **Dynamic Device** in future labs).

#### 4. Add Members
- Selected **Members** > **Add members**.
- Chose the required licensed users (e.g., `User1`).
- Confirmed selections and clicked **Create**.

**Result:** A new security group named **Intune Licensed Users** was successfully created and includes the specified members.

---

### Verification
- Confirmed the new group is listed under **Groups** in the Intune Admin Center.
- Verified that **User1** appears as a member.
- Checked group details such as **Group type** and **Membership type**.

---

### What I Learned
- The role of groups in targeting and managing users or devices in Intune.
- How to create and configure a security group.
- The difference between **Assigned**, **Dynamic User**, and **Dynamic Device** membership types.
- How groups integrate with Intune policies and assignments.

---

### Tools Used
- Microsoft Intune Admin Center  
- Microsoft Entra Admin Center 