# Business case: live quizzes for the IT department

## 1. Problem
Lecturers mark quiz papers by hand and students get feedback days later. Assumptions:
- lecturers running quizzes: 10
- marking time saved per lecturer per week: 1 h
- teaching weeks per year: 30 (so 10 x 1 x 30 = 300 h per year)
- notional value of one hour: 10 USD (students are unpaid; used to compare) (300 h x 10 USD = 3,000 USD per year)

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A | Do nothing | 0 USD | 0 USD | 0 USD |
| B | Buy a Kahoot-like SaaS for 10 lecturers at 15 USD per lecturer per month (assumption, not a researched price) | 0 USD | 1,800 USD | 3,000 USD |
| C | Build Realtime Quiz: 490 h x 10 USD notional effort, hosting 25 USD per month | 4,900 USD | 300 USD | 3,000 USD + 1,800 USD fee avoided |

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|---------------------------|
| B | 3,000 - 1,800 = 1,200 USD | 0 (no one-off cost) | 1,800 - 1,080 = 720 USD per year |
| C | 3,000 + 1,800 - 300 = 4,500 USD | 4,900 / 4,500 = 1.09 | 1,800 + 1,080 - 300 = 2,580 USD per year; payback 4,900 / 2,580 = 1.90 |

All amounts and formulas are in `business-case.csv`.

## 4. Benefits not priced
- Learning outcome: the team practises a full delivery cycle with a real sponsor.
- Data ownership: student names and results stay on the department's own server.
- No per-seat limit: more lecturers or students cost nothing extra.

## 5. Risks per option
- A: marking load and late feedback continue; students keep using unvetted free tools.
- B: price rises or per-seat limits; student data stored by a vendor; no control over features.
- C: the campus proxy may block WebSocket (fallback: SockJS); Spring Boot 4 and Spring Security 7 are newer than most tutorials; late answers may race with the closing of a question; Could features may creep into the MVP.

## 6. Recommendation and review gate
Option C. Payback is about 1.1 years with 10 lecturers and 1.9 years with 6, so it pays back within two academic years in both cases, and the department keeps its data and the learning outcome. Option B is cheaper to start, but its benefit is only 1,200 USD per year and it gives no ownership. Review gate: if the week-7 MVP demo fails, buy option B for the next semester and treat the build as a two-semester project.

See also: [project charter](project-charter.md).