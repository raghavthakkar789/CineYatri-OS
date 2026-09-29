# Roles and Access Control

CineYatri OS begins with three primary roles:
1. Admin
2. Manager
3. Employee

Roles should map to granular permissions rather than hard-coding every check directly to the role name.

## Admin

Admin has organization-wide authority.

Typical permissions:
- Manage employees
- Manage managers
- Manage departments
- Manage clients
- View all projects
- Reassign work
- Manage organization settings
- Manage permissions
- View reporting
- View attendance and leave
- Approve / override leave where configured
- Manage integrations
- Access financial fields where enabled
- View audit logs

Sensitive fields such as salary should have their own permission.

## Manager

Manager controls assigned teams, clients, and projects.

Typical permissions:
- Create / manage assigned projects
- Create and assign tasks
- Manage deadlines
- Schedule shoots
- Assign crew
- Review internal work
- Request revisions
- Send work to client review
- Manage content calendar
- View assigned team workload
- View project progress
- Add internal notes
- Add client-visible notes where permitted

Managers should not automatically see:
- all salaries
- all organization financials
- unrelated private clients
- unrestricted system settings

## Employee

Employees get a focused execution interface.

Typical permissions:
- View assigned tasks
- Update permitted task states
- Start / pause / complete work
- Upload files
- Submit work for review
- View revision feedback
- Comment
- View assigned shoots
- Update assigned shot-list items
- Clock in / out
- Request leave
- View own attendance
- View own performance data

Employees should not automatically see:
- unassigned clients
- other employees' salary information
- organization-wide reports
- system permissions
- private management notes

## Future sub-roles
- Video Editor
- Videographer
- Photographer
- Motion Designer
- Graphic Designer
- Social Media Executive
- Copywriter
- Account Manager
- Creative Director
- Production Manager

These are job/capability labels while authorization remains permission-driven.

## Permission examples
- client.read / create / update / archive
- project.read / create / assign / update / archive
- task.read / create / assign / update / complete
- media.upload / review / approve_internal / send_client_review / approve_client
- shoot.create / assign_crew / update / view
- attendance.clock_self / read_team / edit
- leave.request / approve_team / override
- employee.read / manage / salary.read
- settings.manage
- audit.read

## Authorization rule
Every protected operation should answer:
1. Does this user have the permission?
2. Is the resource inside their organization?
3. Is the resource inside their permitted client/project/team scope?
