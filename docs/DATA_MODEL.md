# Initial Domain Model

This is the first-pass domain model, not the final database schema.

## Organization and identity

### Organization
- id
- name
- status
- created_at

### User
- id
- organization_id
- name
- email
- password_hash / auth identity
- status
- last_login_at

### Role
- id
- organization_id
- name

### Permission
- id
- code

### UserRole
- user_id
- role_id

### RolePermission
- role_id
- permission_id

## Team

### EmployeeProfile
- id
- user_id
- employee_code
- department_id
- manager_user_id
- joining_date
- employment_status
- job_title

### Department
- id
- organization_id
- name

### Skill
- id
- organization_id
- name

### EmployeeSkill
- employee_id
- skill_id
- proficiency

## Clients

### Client
- id
- organization_id
- name
- legal_name
- status
- account_manager_user_id

### ClientContact
- id
- client_id
- name
- email
- phone
- title

### Brand
- id
- client_id
- name
- website
- notes

### BrandAsset
- id
- brand_id
- type
- name
- storage_key / external_url

### Retainer
- id
- client_id
- start_date
- end_date
- status

### RetainerDeliverable
- id
- retainer_id
- deliverable_type
- planned_quantity
- delivered_quantity

## Projects and work

### Project
- id
- organization_id
- client_id
- name
- project_type
- manager_user_id
- status
- start_date
- due_date

### ProjectMember
- project_id
- user_id
- role_label

### Task
- id
- organization_id
- client_id
- project_id
- parent_task_id
- title
- description
- assignee_user_id
- manager_user_id
- priority
- status
- start_at
- due_at
- estimated_minutes
- actual_minutes

### TaskDependency
- task_id
- depends_on_task_id

## Production

### ContentItem
- id
- organization_id
- client_id
- project_id
- title
- content_type
- platform
- status
- owner_user_id
- scheduled_at
- published_at
- published_url

### Script
- id
- content_item_id
- version
- hook
- body
- cta
- status

### Shoot
- id
- organization_id
- client_id
- project_id
- title
- location
- call_time
- start_at
- end_at
- status

### ShootCrew
- shoot_id
- user_id
- crew_role

### Shot
- id
- shoot_id
- content_item_id
- title
- description
- sort_order
- status

## Media and review

### MediaAsset
- id
- organization_id
- client_id
- project_id
- content_item_id
- media_type
- storage_key
- mime_type
- size_bytes

### MediaVersion
- id
- media_asset_id
- version_number
- storage_key
- uploaded_by
- created_at
- approval_status

### ReviewComment
- id
- media_version_id
- author_user_id
- visibility
- timestamp_ms
- body
- resolved_at

### Approval
- id
- content_item_id / media_version_id
- stage
- decision
- decided_by
- decided_at

## Social

### SocialAccount
- id
- client_id
- platform
- handle
- status

### PublishingRecord
- id
- content_item_id
- social_account_id
- caption
- hashtags
- scheduled_at
- published_at
- published_url
- status

## People operations

### AttendanceRecord
- id
- employee_id
- work_date
- clock_in_at
- clock_out_at
- status

### LeaveRequest
- id
- employee_id
- leave_type
- start_date
- end_date
- reason
- status
- reviewed_by

## System

### Notification
- id
- user_id
- type
- title
- body
- read_at

### AuditEvent
- id
- organization_id
- actor_user_id
- action
- entity_type
- entity_id
- metadata
- created_at

## Modeling rules
- All client/project/content queries must be organization-scoped.
- Internal and client-visible comments are explicitly distinguished.
- Media versions should be immutable.
- Business-critical records should generally use soft-delete/archive states.
- Sensitive fields require field-level authorization where appropriate.
