# Access Control List

## [5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

1. What is Role Based Access Control (RBAC) and why do we care?

Role-Based Access Control (RBAC) is a method of managing and enforcing permissions in a system based on roles of individual users within an enterprise. In this approach, permissions are associated with roles, and users are assigned to different roles. This system makes it easier to manage the permissions that users have within a system. We care about RBAC because it simplifies managing user permissions, makes the system more secure by limiting access rights, and allows for easy auditing of user permissions.

2. Describe a Role/Permission heirarchy that you might implement using RBAC.

Consider a business organization with roles such as 'Employee', 'Manager', and 'Admin'.

'Employee' role might have permissions to read documents, submit requests, and write on their personal workspace.
'Manager' role would have all the permissions of an 'Employee' plus the ability to approve requests, manage team members, and access team performance reports.
'Admin' role would have global permissions, including the ability to add/remove users, assign roles, modify permissions, and access all data across the organization.

3. What approach might you take to implement RBAC?

Identify the roles: Determine the various roles in your organization or system.
Define permissions: Identify what actions each role should be able to perform in the system.
Assign roles to users: Allocate users to the appropriate roles based on their responsibilities.
Enforce access control: In the system's code, enforce access control by checking a user's role and its permissions before allowing an action.
Review and modify: Periodically review the roles and permissions to make sure they still align with the needs of the organization.


## [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

1. If Authentication is “you are who you say you are,” what is Authorization?

If authentication is about verifying the identity of a user, authorization is about verifying what that user has permissions to do. Once a system knows who a user is (authentication), it needs to know what that user is allowed to do, i.e., the resources they can access or actions they can perform (authorization).

2. Name three primary rules defined for RBAC.

- Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
- Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.
- Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.

3. Describe RBAC to a non-technical friend.

When you log into a website, you're assigned a "role" (like the wristband) based on your job or the reason you're using the site. That role determines what parts of the site you can access and what you can do there.


## [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

1. What Are access rights Associated with? The User? or The Role? Explain.

Access rights in RBAC are associated with the role, not the individual user. For instance, instead of giving each employee at a company permission to view a certain document, you would give that permission to the "Employee" role. Then any user assigned to the "Employee" role would have that permission.

2. Access Rights, or Authorization, is activated after a user successfully does what?

Access rights or authorization is activated after a user successfully authenticates. In other words, they've proven their identity (like entering a correct username and password).

3. Explain how RBAC might benefit a business.

RBAC can greatly simplify the management of permissions. Instead of tracking what each individual user can do, admins can manage roles and then assign users to these roles. This approach is often easier to manage at scale and can help prevent errors, like giving a user access to a system they shouldn't have. It can also help increase security by ensuring users only have the access they need to do their jobs (a principle known as "least privilege").