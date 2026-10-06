# Ideal customer profile

One sentence: Series B or later companies whose buyer is a head of GTM, growth or RevOps.

If a company does not have someone who owns the revenue number and loses sleep over the forecast, we have
nothing to sell them. Everything below is a way to find that person's company faster.

## Qualifiers

- **Stage.** Series B, Series C, Series D, growth-stage or public. Series B is where a founder stops running
  sales from a spreadsheet and hires the person we sell to. Bootstrapped companies qualify only if they
  are clearly past that size (50+ quota carriers).
- **What they sell.** B2B software with a sales team: SaaS, developer tools, data and analytics,
  security, fintech, martech, HR tech, cloud infrastructure, enterprise software. The buyer exists in
  these companies.
- **Size.** Sweet spot 100 to 2,000 employees, 10 to 300 quota carriers. Below 100 the forecast fits in
  a spreadsheet. Above 2,000 we are usually displacing an incumbent and the cycle doubles.
- **Motion.** Sales-led or hybrid. Pure product-led companies with no quota carriers rarely renew.
- **Geography.** France, UK, DACH, Nordics, Benelux, US east coast. We sell in English and French.

## Disqualifiers

- Pre-seed, seed, Series A. We have tried; they churn when the first VP Sales leaves.
- Agencies, IT services, consultancies, systems integrators. Project revenue, not pipeline.
- Companies that do not sell software: manufacturing, logistics, retail, consumer goods, banks, insurers,
  energy, telcos, hospitality, healthcare providers, schools. Some have sales teams; none forecast the way
  we model it.
- Marketplaces and consumer apps.
- Subsidiaries where the revenue org sits with the parent. Sell to the parent.

## How we score (Q4 version)

Tier A: ICP and 200+ employees. Priya works these personally, Tom supports.
Tier B: ICP and under 200 employees, or employee count unknown. Tom's outbound.
Tier C: not ICP. Nurture only, no outbound.

Scoring runs on `funding_stage` and `industry` in `data/accounts.csv`, then size. Both fields are patchy,
which is why enrichment is initiative 1 for the quarter.
