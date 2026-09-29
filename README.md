# CineYatri OS

CineYatri OS is a specialized operating system for creative agencies, video production teams, editors, social-media managers, managers, and administrators.

## Product vision

Manage the full creative lifecycle in one system:

Client → Campaign / Project → Content Plan → Pre-production → Shoot → Post-production → Internal Review → Client Review → Approval → Schedule → Publish → Analytics

## Primary roles

- **Admin** — company-wide control, people, clients, permissions, reporting, finance visibility, system settings.
- **Manager** — projects, team assignments, shoots, reviews, deadlines, client approvals, workload.
- **Employee** — assigned work, shoots, uploads, revisions, attendance, leave, comments, delivery.

## Core modules

1. Authentication & RBAC
2. Employee management
3. Client & brand workspaces
4. Projects & campaigns
5. Tasks, subtasks & dependencies
6. Content production pipeline
7. Shoot planner
8. Scripts & shot lists
9. Post-production review
10. Video versioning
11. Time-coded feedback
12. Client approval portal
13. Social content calendar
14. Publishing workflow
15. Notifications
16. Attendance & leave
17. Search & activity logs
18. Dashboards & reporting

## Product principles

- Built for creative production, not generic task management.
- Client, Project, Content, Shoot, Review, and Publishing are first-class objects.
- Keep internal comments separate from client-visible comments.
- Measure delivery, quality, and reliability — not invasive employee surveillance.
- Build integrations before recreating mature tools such as accounting, email, or full video editing.

## Repository structure

```
docs/
  PRODUCT_SPEC.md
  ARCHITECTURE.md
  RBAC.md
  DATA_MODEL.md
  ROADMAP.md

apps/
  web/
  api/
```

The `apps/` directories are reserved for the application implementation once the product and architecture foundation is finalized.

## Status

**Phase 0 — Product definition and architecture**

See the `docs/` directory for the current specification.
