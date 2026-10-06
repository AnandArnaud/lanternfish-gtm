# Weekly pipeline review

Monday 09:30 Paris, 45 minutes, Daniel runs it. Priya, Tom, Léa attend. Agenda is fixed; if a topic does
not fit, it goes to Thursday.

## Before the meeting (Léa, Friday)

Export deals and accounts from the CRM into `data/`. Flag: deals past close date, deals with no activity in
14 days, accounts with no activity in 90 days that still sit in sql or opportunity, customers meeting the
churn-watch rule, duplicate accounts found this week.

## In the meeting

1. The number. Commit, best case, pipeline coverage for the quarter. 5 minutes.
2. Deals that moved. Every deal that changed stage or close date, with a sentence from Priya. 15 minutes.
3. Stale pipeline. Past-due and no-activity deals: close, push or keep with a reason. 10 minutes.
4. Churn watch and expansion. Flagged customers and seat candidates. 10 minutes.
5. Data. Duplicates merged, enrichment progress, anything that changed a number. 5 minutes.

## After the meeting

Daniel updates `plan/2026-q4.md` if the target or an initiative changed. Changes to the CRM happen on
Monday afternoon, by Léa, from the meeting notes, never during the meeting.

## Rules

Nobody edits a close date during the meeting. A deal with no next step is not in commit. A customer in
churn watch two weeks running gets a named owner and a date.
