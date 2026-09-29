# Product Specification

## 1. Core workflow

CLIENT → BRAND → CAMPAIGN / PROJECT → CONTENT PLAN → PRE-PRODUCTION → SHOOT → POST-PRODUCTION → INTERNAL REVIEW → CLIENT REVIEW → APPROVED → SCHEDULED → PUBLISHED → ANALYTICS / REPORT

## 2. Client workspace

Each client should have:
- Company / brand profile
- Contact people
- Social accounts
- Website
- Account manager
- Assigned creative team
- Retainer / contract period
- Monthly deliverables
- Brand guidelines
- Logos, fonts, colors, reference links
- Projects
- Content calendar
- Shoots
- Approvals
- Reports
- Notes

### Retainer tracking
Track planned vs delivered content:
- Reels
- Static posts
- Carousels
- Stories
- Shoots
- Other custom deliverables

## 3. Projects and campaigns

Supported project types may include:
- Monthly social-media management
- Brand film
- Corporate film
- Product shoot
- Event coverage
- Advertisement
- Reel campaign
- Influencer campaign
- YouTube production

Project records should include:
- Client
- Manager
- Team
- Dates
- Status
- Progress
- Deliverables
- Budget / cost fields (later phase)
- Attachments
- Notes

## 4. Creative content pipeline

Replace generic To Do / Doing / Done with production-specific states:

IDEA → SCRIPTING → SCRIPT APPROVAL → SHOOT PLANNED → SHOT → FOOTAGE UPLOADED → EDITING → INTERNAL REVIEW → INTERNAL REVISION → CLIENT REVIEW → CLIENT REVISION → APPROVED → SCHEDULED → PUBLISHED

The pipeline should be configurable by project template later.

## 5. Shoot planner

A shoot should support:
- Client / project
- Date and time
- Location
- Call time
- Crew
- Roles
- Equipment
- Content to capture
- Shot lists
- Call sheet
- Notes
- Status

Future enhancement: mobile-friendly shot completion during a shoot.

## 6. Script and shot-list management

Scripts:
- Hook
- Scene breakdown
- Voice-over / dialogue
- Visual notes
- CTA
- Approval state

Shot lists:
- Shot title
- Shot type
- Description
- Required equipment
- Talent / product
- Completion status
- Notes

## 7. Post-production

Each video/content item should support:
- Assigned editor
- Version history
- Duration
- Current status
- Uploaded files
- Internal comments
- Client-visible comments
- Time-coded review notes
- Approval state

Version naming should be system-managed, e.g. MN_REEL_014 / V1 / V2 / V3 / V4 — APPROVED.

## 8. Client approval portal

Clients should not enter the internal employee system.

Provide a restricted approval view where the client can:
- Preview assigned content
- Approve
- Request changes
- Comment
- Review previous versions where allowed

Clients must never see:
- Internal notes
- Employee data
- Internal performance data
- Other clients
- Private business information

## 9. Social media management

Content calendar filters:
- Client
- Platform
- Content type
- Status
- Owner
- Campaign

Publishing record:
- Platform
- Caption
- Hashtags
- Location
- Mentions / collaborators
- Audio
- Thumbnail
- Scheduled time
- Published URL
- Publish status

## 10. Task management

Task fields:
- Title
- Client
- Project
- Content item
- Assignee
- Manager
- Priority
- Status
- Start date
- Deadline
- Estimate
- Actual time
- Attachments
- Checklist
- Dependencies
- Comments

Priorities: Urgent, High, Normal, Low.

## 11. Workload

Managers should see team capacity and active assignments so work is distributed intentionally.

Avoid reducing workload to a single simplistic score. Capacity should consider task count, estimate, deadlines, and assignment dates.

## 12. Attendance and leave

Employee self-service:
- Clock in / out
- Daily hours
- Monthly attendance
- Leave request
- Leave balance
- WFH / half-day where permitted

Attendance methods can later support:
- Office IP
- GPS
- QR
- Mobile

## 13. Performance

Use work outcomes instead of surveillance.

Useful metrics:
- Tasks completed
- On-time delivery
- Average revision rounds
- Average cycle time
- First-pass internal approval
- First-pass client approval
- Reopened work

Do not use mouse movement, keyboard activity, random screenshots, or online-time as primary performance indicators.

## 14. Search and command palette

Global search should cover clients, employees, projects, tasks, content, shoots, assets, and campaigns.

## 15. Automations

Examples:

### Approved content
When content becomes Client Approved:
1. move to Ready to Publish
2. notify the social-media manager
3. create publishing task

### Shoot reminder
When a shoot is tomorrow:
1. notify crew
2. surface call sheet
3. validate equipment checklist

## 16. Templates

Initial templates:
- Reel production
- Product shoot
- Monthly social-media management
- Brand / corporate film

## 17. Deferred features

Do not build these in V1:
- Full accounting
- Full payroll
- Full sales CRM
- Full email client
- Browser video editor
- Canva replacement
- Premiere replacement
- AI video generation suite
- Invasive employee monitoring
