# Post-mortem: CampusPay wallet (fictional case from Lab-01)

## 1. Timeline and sources
| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Start of semester | University asks IT to build a cashless app for canteen and library fines in one semester | fictional case from Lab-01 |
| 2 | Start | Head of finance "sponsors" it by e-mail and never attends a review | fictional case from Lab-01 |
| 3 | Start | Lead developer acts as PM and coder; success is defined as "launch in September" | fictional case from Lab-01 |
| 4 | After the survey | Scope grows to bus tickets and parking | fictional case from Lab-01 |
| 5 | Before launch | No test with real card terminals is run | fictional case from Lab-01 |
| 6 | Launch day | Terminals reject 40 % of payments and the canteen queue doubles | fictional case from Lab-01 |
| 7 | Day 3 | App is withdrawn | fictional case from Lab-01 |
| 8 | Five months later | Relaunch for the canteen only | fictional case from Lab-01 |

## 2. Classification and organisation
Project / programme: a single project, although the later scope (canteen, library, bus, parking) looked like a programme of related projects with no programme management. Structure and PM authority: the PM was also the lead developer, so authority was low and divided between managing and coding. Sponsor, charter, PMO: the sponsor existed only by e-mail and never attended a review; there was no charter and no PMO.

## 3. Success criteria
Stated: "launch in September". Missing measurable criteria: payment success rate, queue time, number of transactions per hour, a tested go-live checklist. Ignored dimensions (benefits, users, operations, team): the benefit for canteen users, the readiness of the card-terminal operations, and a team doing two jobs.

## 4. Process groups and knowledge areas
| Process group              | What went wrong or was skipped |
|----------------------------|--------------------------------|
| Initiating                 | No charter; the head of finance never accepted the sponsor role, so nobody could refuse the bus-ticket scope. |
| Planning                   | No scope baseline or test plan; requirements grew after a survey. |
| Executing                  | Features were added without integration work with real card terminals. |
| Monitoring and controlling | Progress was reported as on schedule without a single end-to-end test; scope changes were not controlled. |
| Closing                    | The app was withdrawn after three days and no lessons-learned record exists. |

Knowledge areas most responsible: scope management (it grew from canteen to bus tickets and parking without approval), quality management (no test with real terminals, 40 % of payments rejected) and stakeholder management (the sponsor was absent, and the terminal operators were never involved).

## 5. Ethics
Decision examined: launching on day one without testing on real terminals. Responsibility: the team owed users a working payment system and ignored the risk. Respect: students and canteen staff were exposed to failed payments and queues. Fairness: the cost of the failure fell on users who had no say. Honesty: reporting "on schedule" without end-to-end evidence misled the sponsor.

## 6. What our project will do differently
| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will run a live session with 100 simulated students on the real campus network before the pilot | load test report with 0 errors | 12 | O4, milestone week 12 |
| 2 | We will hold a signed charter with a named sponsor who attends the week-7 and week-13 gates | signature on the charter and gate minutes | 1 | section 10 approval, authority clause |
| 3 | We will accept no new scope without the sponsor's written approval | change-log entries with approval within 5 working days | 14 | section 9 authority, out-of-scope list |
| 4 | We will judge success by numbers, not by a launch date | objectives O1-O5 reviewed at each gate | 7 | section 2 objectives |
| 5 | We will keep line coverage at 80 % or above, checked by CI on every merge | CI report | 4 | O5 |