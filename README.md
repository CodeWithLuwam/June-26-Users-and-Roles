# ServiceNow: Managing Users, Roles, and Groups

This guide explains how to create and manage users, assign roles, and configure groups in ServiceNow. It also demonstrates best practices for assigning permissions via groups instead of individual users.

## Table of Contents
1. [Overview](#overview)
2. [Create or View a User](#create-or-view-a-user)
3. [Understand Roles, Permissions, and Groups](#understand-roles-permissions-and-groups)
4. [Find and Manage Groups](#find-and-manage-groups)
5. [Example: Assign Catalog Admin Role to a Group](#example-assign-catalog-admin-role-to-a-group)
6. [Best Practices](#best-practice)

<a name="overview"></a> 
## 1. Overview
In ServiceNow:
- **Permissions = Roles**
- **Roles are collections of permissions** (e.g., create, read, update, delete).
- **Groups contain roles**, and users inherit roles by being members of groups.
- Assigning roles via groups allows for **scalability and easier management**.

<a name="create-or-view-a-user"></a>
## 2. Create or View a User
1. Navigate to **All Menu → User Administration → Users**.
2. Click on **Users**.
3. To **view an existing user**, click the user record (e.g., *Abel Tuter*).
4. To **create a new user**, click **New** and fill out the required details.

### User Record Details
- The **Groups** tab shows which groups the user belongs to.
- The **Roles** tab shows roles assigned directly to the user.
- Users can have roles from:
  -   Their groups
  -   Additional roles assigned individually.

<a name="understand-roles-permissions-and-groups"></a>
## 3. Understand Roles, Permissions, and Groups
- **Roles** = Define what actions (create, read, update, delete) and what data or applications the user can access.
- **Groups** = Logical collections of users that share similar responsibilities.
- Roles can be:
  - Assigned directly to users.
  - Assigned through groups (preferred method).
>Best Practice: Assign roles via groups for easier scalability and centralized management.

<a name="find-and-manage-groups"></a>
## 4. Find and Manage Groups
1. Navigate to **All Menu → User Administration → Groups**.
2. Search for a specific group (e.g., `Service Desk`).
3. Click the group record to view:
   - **Manager** (e.g., *Beth Anglin*).
   - **Roles assigned to the group** (e.g., `itil`, `service_viewer`).
   - Group members (users who inherit these roles).

>Note:
>Even if a group has only 2 roles, an individual user may have more roles from other groups or direct assignments.

<a name="example-assign-catalog-admin-role-to-a-group"></a>
## 5. Example: Assign Catalog Admin Role to a Group
We will assign a catalog_admin role to the group `Catalog Request Approvers for Sales`.
### Steps:
1. Go to **All Menu → Groups**.
2. Search for **Catalog Request Approvers for Sales** and open the record.
3. Under **Roles**, click **Edit**.
4. Remove the `catalog` role (view-only).
5. Add the **catalog_admin** role (gives configuration privileges).
6. Click **Save**.

## Test the Changes
1. Impersonate a group member (e.g., *Don Goodlife*).
2. Navigate to **Service Catalog → Items**.
3. Confirm that the user can now **edit catalog items**.

<a name="best-practice"></a>
## 6. Best Practices
- Use **least privilege** principle: Assign only the roles needed for the job.
- Prefer **group-based role assignments** over individual role assignments.
- Review roles and groups periodically for security and compliance.

## Additional Notes
- **Parent-Child Relationships**: A manager role typically includes permissions that all child roles have.
- **UI Variations**: Users may have different workspaces based on roles (e.g., agents use a ticket-focused workspace).
- Always **document any role changes** for auditing purposes.
