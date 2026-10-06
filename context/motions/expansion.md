# Expansion

Owner: Priya, with Léa for the data. Expansion was 31% of new ARR in H1 and should be 40% in Q4.

## Three plays

**Seats.** Customers using more than 80% of purchased seats, healthy, logging in weekly. Offer the next
seat tier before renewal, not at it. Candidates are visible in `data/accounts.csv` from `seats_used`,
`seats_purchased`, `health_score` and `last_login_days`.

**Regions and subsidiaries.** When a customer is one entity of a group, map the group and sell to the
siblings with the parent's reference. `parent_company` in the CRM is filled for some subsidiaries and not
others; Léa keeps a manual list that should become a proper field.

**Champion moves.** When a champion changes company, we reach out within two weeks with a note from their
old leader. Historically a 40% meeting rate. Tracked by hand on Fridays, which is the weakest part of the
whole motion.

## Churn watch

Customers with health under 45, no login in a month, or seat use under half of purchase are flagged in the
Monday review and get a call from Priya that week. Three customers churned in Q3; two had been flagged and
one had not, because their health score was stale. Churn-risk flagging should run on the data, not on
memory.
