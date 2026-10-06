# ADR 0001: GTM tooling is undecided

Status: open. Date: 2026-10-06. Owner: Léa.

## Context

Everything in `plan/2026-q4.md` needs the same capabilities: deduplicate accounts, fill missing domains and
employee counts, find and verify work emails for named people, build lists by country, size and industry,
score accounts against the ICP and against closed-won, detect signals, and read and write the CRM with an
audit trail. Today it is spreadsheets, a few scripts of Léa's, and Tom's Friday afternoons.

## What we considered so far

Building it in-house on the warehouse (we do not have an engineer to spare), one of the all-in-one GTM data
platforms, a stack of single-purpose tools glued with scripts, or a contractor. Nothing has been trialled on
our actual data yet.

## Decision

None. Any proposal must be run against `data/accounts.csv`, `data/contacts.csv` and `data/closed_won.csv`
in this repo and come back with: rows deduplicated and how, domains and employee counts filled with
source per field, verified emails for a sample of 50 contacts with the verification method, the ICP and
lookalike scores, and the cost per month at our volume (5,000 accounts now, 10,000 by Q1). Put the
results in `data/` with a suffix and open a PR; the Thursday check-in decides.

## Consequences

Until a decision, nothing writes to the CRM except Léa on Monday afternoons.
