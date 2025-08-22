# ServiceNow: Managing Users, Roles, and Groups

This guide explains how to create and manage users, assign roles, and configure groups in ServiceNow. It also demonstrates best practices for assigning permissions via groups instead of individual users.

## Table of Contents
1. [Overview](#overview)
2. [Create or View a User](#create-or-view-a-user)
3. [Understand Roles, Permissions, and Groups](#understand-roles-permissions-and-groups)
4. [Find and Manage Groups](#find-and-manage-groups)
5. ## Example: Assign Catalog Admin Role to a Group
6. ## Best Practices

<a name="overview"></a> 
## Overview
In ServiceNow:
- Permissions = Roles
- Roles are collections of permissions (e.g., create, read, update, delete).
- Groups contain roles, and users inherit roles by being members of groups.
- Assigning roles via groups allows for scalability and easier management.

<a name="create-or-view-a-user"></a>
## Create or View a User
1. Navigate to **All Menu → User Administration → Users**.
2. Click on **Users**.
3. To **view an existing user**, click the user record (e.g., Abel Tuter).
4. To **create a new user**, click **New** and fill out the required details.

### User Record Details
- The **Groups** tab shows which groups the user belongs to.
- The **Roles** tab shows roles assigned directly to the user.
- Users can have roles from:
  -   Their groups
  -   Additional roles assigned individually.

<a name="understand-roles-permissions-and-groups"></a>
## Understand Roles, Permissions, and Groups
- **Roles** = Define what actions (create, read, update, delete) and what data or applications the user can access.
- **Groups** = Logical collections of users that share similar responsibilities.
- Roles can be:
  - Assigned directly to users.
  - Assigned through groups (preferred method).
>Best Practice: Assign roles via groups for easier scalability and centralized management.

<a name="find-and-manage-groups"></a>
## Find and Manage Groups
1. Navigate to **All Menu → User Administration → Groups**.
2. Search for a specific group (e.g., `Service Desk`).
3. Click the group record to view:
   - **Manager** (e.g., *Beth Anglin*).
   - **Roles assigned to the group** (e.g., `itil`, `service_viewer`).
   - Group members (users who inherit these roles).

>Note:
>Even if a group has only 2 roles, an individual user may have more roles from other groups or direct assignments.
