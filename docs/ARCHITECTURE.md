# Architecture

CineYatri OS should start as a modular monolith with clear domain boundaries. This keeps development fast while preserving a future path to split heavy services such as media processing, notifications, social publishing, or analytics.

## Suggested application shape

Browser / Mobile Web → Web App → API

API domains:
- Auth & RBAC
- Organization
- Clients
- Projects
- Tasks
- Production
- Reviews
- Social
- People
- Attendance / Leave
- Notifications
- Reporting

Infrastructure:
- PostgreSQL
- Object Storage
- Background Jobs
- External Integrations

## Recommended implementation direction

### Web
- Next.js
- React
- TypeScript
- Tailwind CSS
- Server-side authorization checks for protected routes

### API
Choose one backend and keep it independent from the web application boundary:
- FastAPI + Python, or
- NestJS + TypeScript

### Data
- PostgreSQL
- Redis later for queues / caching if needed
- S3-compatible object storage for media and documents

### Background processing
Use jobs for:
- Video metadata extraction
- Thumbnail generation
- Notifications
- Report generation
- Social publishing
- Transcription / AI features

## Multi-tenancy
The initial deployment may be single-company, but core tables should carry an organization_id where appropriate so the model is not painted into a corner.

## Authorization
Authorization must be enforced in the API, not only by hiding buttons in the UI.

Use:
- role-based permissions
- resource ownership / assignment checks
- client/project membership checks
- audit logs for sensitive actions

## Media
Do not store large videos directly in PostgreSQL.

Store:
- media metadata in PostgreSQL
- video/image files in object storage
- signed URLs for controlled access

For versioned media, preserve immutable versions and point the content item to the active version.

## Comments
Comments need an explicit visibility field:
- INTERNAL
- CLIENT_VISIBLE

Never infer visibility from author role.

## Client approval access
Use a separate client-facing permission boundary. A secure approval token or authenticated client portal can be added depending on deployment needs.

## Notifications
Design notifications around events such as:
- task assigned
- deadline approaching
- revision requested
- content approved
- shoot upcoming
- client commented
- leave decision

## Audit logging
Log important changes:
- role / permission changes
- client access changes
- content approval changes
- task reassignment
- deletions
- attendance edits
- leave decisions

## Security baseline
- Secure session handling
- CSRF protection where applicable
- Strong password hashing
- Rate limiting
- Input validation
- Signed media access
- Least-privilege permissions
- Audit trail
- Secrets outside source control
