# Lanternfish GTM

This repo is how the go-to-market team at Lanternfish works. If it is not in here, it is not the plan.

## Who we are

Lanternfish sells pipeline forecasting to revenue leaders. A VP Sales or a RevOps lead connects their CRM,
and we tell them which deals will actually close this quarter, which reps are sandbagging, and how far the
board number is from reality. Founded in Paris in 2023, Series A (June 2025), 34 people, customers in
France, the UK, the Nordics, Germany and the US east coast. ARR is just under EUR 3M.

We sell to companies that have a real sales organisation to forecast: Series B and later, usually 100 to
2,000 employees, selling B2B software. The buyer is the person who owns the number: a head of GTM, a head
of growth or a head of RevOps. Details in [context/icp.md](context/icp.md).

## The GTM team

Four people. Everyone touches the pipeline.

| who | role | owns |
|---|---|---|
| Daniel Okafor | Head of GTM | the plan, the number, this repo |
| Priya Natarajan | Account Executive | every opportunity from first demo to signature |
| Tom Oakes | SDR | outbound, inbound response, list building |
| Léa Marchand | RevOps | the CRM, the data, the weekly forecast, tooling |

CRM of record: HubSpot. Two reps who left this year (Sofia Lindqvist in March, Marcus Reed in July) still own
records in the CRM; reassignment is on the Q4 plan.

## GTM as code

We lost most of H1 to decisions that lived in Slack threads and Notion pages nobody could find. From Q3 the
rule is: the ICP, the personas, the plays, the plan, the review cadence and the data all live here, as text
and CSV, and every change goes through a pull request. A change to the ICP is a diff that Daniel reviews.
A new outbound play is a file under `context/motions/`. A decision is an ADR under `docs/decisions/`.

The tooling question is deliberately open. We know what we need (enrichment, dedupe, list building,
scoring, something that can read and write the CRM) and we have not picked how to do it. See
[docs/decisions/0001-gtm-tooling.md](docs/decisions/0001-gtm-tooling.md). Proposals welcome as PRs; show
your work on the data in `data/`.

## Layout

```
context/      who we sell to and why: icp.md, personas/, jobs.md, objections.md, proof.md, signals.md
context/motions/   outbound, inbound, expansion: the plays we run
plan/         the quarterly plan (plan/2026-q4.md is current)
cadence/      recurring meetings and what they look at
initiatives/  one file per in-flight initiative (see initiatives/README.md)
docs/decisions/   ADRs
data/         CRM exports, see below
```

## data/

Exports from the CRM, taken 2026-10-06. They are as messy as the CRM is; that is the point of keeping them
here. Do not hand-edit them. If you clean something, write the cleaned file next to it with a suffix
(`accounts.clean.csv`) and describe the method in the PR.

| file | rows | notes |
|---|---|---|
| `data/accounts.csv` | 5,000 | company/account object. Known problems: duplicates, blank domains, two LinkedIn columns that disagree, country spelled five ways, employee count missing on a fifth of rows |
| `data/contacts.csv` | 300 | people we know at those accounts. No email column: the previous export tool stripped it and nobody re-added it |
| `data/deals.csv` | 200 | open pipeline |
| `data/closed_won.csv` | 50 | every customer we have closed, with ARR and what they bought us for |
| `data/prospects.csv` | 5,000 | not a CRM export: the list Tom bought from a list vendor in September. Company name and domain, nothing else. Roughly a tenth are already in the CRM; nobody has qualified any of it yet |

Column notes for `accounts.csv`: `lifecycle_stage` is lead/mql/sql/opportunity/customer/churned.
The seat, health, login, ticket and ARR columns are only filled for customers. `parent_company` is only
filled for subsidiaries of a group, and not consistently. `last_activity_date` is the last logged touch of
any kind.
