# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | It ends with the week-14 pilot and delivers a product that did not exist before. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | It repeats every night with the same output and no end date. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | It has a fixed deadline and happens once, leaving a new hosting setup. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | Each ticket has a deadline, but the service itself never ends. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | Three related projects deliver the shared login and grade export, a benefit none gives alone. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | The same routine repeats every month with no end date. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | It is a new capability with its own scope and end, once funded separately. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | It is an ongoing service with no end date, run day after day. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | Each edition has a deadline of 31 January and produces a new document. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | It must finish within the summer break and is a one-time replacement. |

## Grey zones
- **Row 6 (monthly patches).** It repeats every month, so it looks like an operation, but each patch round has its own list and a start and end. Knowing whether the department authorises and budgets each round separately, with a defined "done", would settle it.
- **Row 9 (annual IT report).** It repeats every year, yet each report is unique and has a hard deadline. If the department funds each edition as its own endeavour with a named owner and an end date it is a small project; if it is routine annual work with no separate budget it is an operation.

## What our project hands over
At go-live in week 14, Realtime Quiz is handed over to IT operations, who run the VPS at gicitc.com, the backups and the monitoring, and to the lecturers who use it for their quizzes. IT operations need a runbook, a deployment checklist with the docker-compose production file, and a working backup job at least two weeks before the pilot. Lecturers need a short user guide, and the team must stay available for fixes until the hand-over is accepted at the week-13 gate.