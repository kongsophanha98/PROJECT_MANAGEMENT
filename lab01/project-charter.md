# Project charter: Realtime Quiz platform

| Field | Value |
|-------|-------|
| Version | 1.0 (draft for sponsor approval) |
| Date | 2026-09-29 |
| Sponsor | Head of the IT department |
| PM | Mr. Tongsreng, supervising lecturer |

## 1. Purpose and justification
Lecturers in the department mark quizzes by hand, about 300 hours per year in total, and students only see their results days later. The Realtime Quiz platform lets an instructor author multiple-choice quizzes and run live, timed sessions where students join with a 6-character code and see their score and a leaderboard at once. The benefit is saved marking time, instant feedback and student data that stays on the department's own server. The comparison of doing nothing, buying a quiz service or building it, with a payback of about 1.1 years for building, is in [business-case.md](business-case.md).

## 2. Objectives and success criteria
| # | Objective (what will be true) | Success criterion (number + week) |
|---|-------------------------------|-----------------------------------|
| O1 | An instructor can run a complete live quiz with all Must features | 8 of 8 Must features pass in a live MVP demo, week 7 |
| O2 | Real students use the platform in a live class | One pilot session with 50 students and 0 blocking defects, week 14 |
| O3 | Scores and questions reach every screen quickly | Broadcast latency of 500 ms or less at the 95th percentile, measured in the pilot, week 14 |
| O4 | The server copes with a full class | Load test with 100 simulated students and 0 errors, week 12 |
| O5 | The code stays tested and releasable | Line coverage of 80 % or more and CI green on every merge, from week 4 to week 14 |

## 3. High-level scope
In scope:
- Quiz editor with multiple-choice questions and a timer per question
- Live session with joining by code and a server-controlled timer
- Instant scoring, feedback and leaderboard
- Accounts and roles for instructors, students and guests
- Responsive web interface for phones and laptops
- Analytics report and CSV/PDF export of results
- Deployment package and runbook for the department's server

Out of scope:
- Native mobile apps
- Question types other than multiple choice
- Video conferencing
- Integration with the learning management system
- Scaling across several server instances

## 4. Milestones
| Week | Milestone | Ends process group |
|------|-----------|--------------------|
| 1 | Charter signed and team formed | Initiating |
| 3 | Project plan baselined, environments and accounts ready | Planning |
| 4 | Quiz authoring finished and coverage check running in CI | Executing |
| 7 | MVP demo: all Must features live | Executing |
| 10 | Analytics and export finished | Executing |
| 12 | Load test with 100 simulated students passed | Monitoring and controlling |
| 14 | Pilot with 50 students and project closure | Closing |

## 5. Budget summary
```
Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h
Cash:    hosting 4 x 25 USD = 100; domain 12; tools 48; reserve 40 (25 % of 160)
         total 200 USD
```

## 6. Assumptions
- Each student can give 8 hours per week for all 14 weeks.
- The campus network lets WebSocket traffic through, or the fallback transport works.
- The department's server at gicitc.com stays available for the whole semester.
- The data protection officer approves storing student names and results before the pilot.

## 7. Constraints
- The project lasts 14 weeks from 2026-09-29 and the pilot takes place in week 14.
- Cash spending is capped at 200 USD.
- The platform runs on one server with 2 vCPU and 2 GB RAM.
- The team uses Spring Boot, PostgreSQL and Docker Compose, as set by the course.
- Student data stays on campus infrastructure.

## 8. High-level risks
- The campus proxy may block WebSocket connections, so the fallback transport must be tested early.
- Spring Boot 4 and Spring Security 7 are newer than most tutorials, which may slow the team.
- Could features may creep into the MVP and put the week-7 demo at risk.

## 9. Project manager authority
The PM may re-plan tasks and move effort between phases as long as the total stays within 490 hours and 200 USD, and does not need approval for that. Any new scope, a change of the week-7 or week-14 dates, or spending from the reserve beyond 40 USD needs the sponsor's written approval, which the sponsor gives or refuses within 5 working days.

## 10. Approval
Sponsor: ____________________  Date: __________
PM:      ____________________  Date: __________