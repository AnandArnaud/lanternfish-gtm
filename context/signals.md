# Signals

Things that happen to a company shortly before it buys us. Ranked by how often they showed up in the
twelve months before a closed-won deal (looked at all 50 in `data/closed_won.csv`, July 2026).

| signal | share of closed-won showing it | what it means |
|---|---|---|
| raised a Series B or later round in the previous 12 months | 68% | new board, new expectations, new VP Sales |
| hiring data engineers or a RevOps analyst | 54% | they are about to try to build it themselves; get in first |
| champion changed jobs into the account | 31% | our best lead source; see expansion motion |
| new VP Sales or CRO in the previous 6 months | 44% | wants their own forecast, not the predecessor's |
| CRM clean-up project announced internally | 22% | usually visible as a RevOps job post that mentions data quality |
| board-level forecast miss (public: guidance cut; private: told to us) | 18% | urgency, short cycle |
| opened a second sales office / region | 20% | roll-up pain multiplies |

## How we track them

Funding and hiring come from a weekly check of announcements and job posts. Champion moves come from
LinkedIn, by hand, on Fridays. We would like all of this automated against `data/accounts.csv`; this is
initiative 3 in the Q4 plan. Whatever we pick has to write the signal, the date and the source back to the
account record, or Léa will not accept it.

## Signals we tried and dropped

Website traffic spikes (noise). Tech-stack detection (told us nothing we could act on). Review-site visits
(too few to matter at our volume).
