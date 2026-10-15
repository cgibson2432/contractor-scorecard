# Versioned class-code and premium benchmark data

## Purpose

Keep pricing reference data separate from the diagnostic UI. Every production rate record must retain its source, effective period, rating basis, and data type. Do not treat a class-code reference as a market quote or imply a customer is overpaying solely because a ratio is above a reference.

## Official California workers' compensation sources

- WCIRB regulatory and pure premium rate filings: https://www.wcirb.com/filings-and-plans/regulatory-and-pure-premium-rate-filings
- WCIRB classification system: https://www.wcirb.com/research-and-education/online-guide-workers%E2%80%99-compensation/standard-classification-system
- California Department of Insurance workers' compensation rate comparison: https://www.insurance.ca.gov/01-consumers/105-type/9-compare-prem/wc-rate/
- CDI rate filings and viewing room: https://www.insurance.ca.gov/0250-insurers/0800-rate-filings/0050-viewing-room/

Use the exact current filing/download and record its effective date. Do not assume that an older downloaded file or previously entered number is current. Confirm class code, official phraseology, any wage-tier or eligibility conditions, and applicable California rules before using a record.

## Data types

1. **Advisory pure premium** — WCIRB advisory benchmark. It is not a carrier's filed rate and is not the insured's final premium.
2. **Carrier filed/manual rate** — a carrier-specific rate/rule record tied to a filing or rating manual and effective dates. It still does not equal final premium.
3. **Observed quote / renewal** — a real Albano quote or renewal, recorded with permission and de-identified where appropriate. This is market evidence, not a universal rate.
4. **Estimated public range** — third-party or modeled range. Keep separate from official data and label its methodology and limitations.

## Templates

- `wc_advisory_rates_template.csv`: import into the diagnostic after a human has reviewed the official source file and normalized its columns to this template.
- `wc_carrier_rates_template.csv`: carrier/class-specific WC rate records. Do not populate without a carrier manual/filing reference and effective dates.
- `gl_rate_observations_template.csv`: quote and renewal observations for GL. GL exposure may be payroll, gross sales, subcontractor cost, area, units, or another defined basis. Do not combine different bases as if directly comparable.

The templates are intentionally header-only. They contain no fabricated or unverified rates.

## WC premium math

A simplified manual premium indication is:

`payroll / 100 × applicable carrier rate`

This is only a starting point. Final premium can be affected by class allocation, experience modification, schedule rating where permitted, carrier rating plans, deductible credits, minimum premium, expense constants, taxes, assessments, and other applicable rules. Preserve the actual rating basis and all relevant adjustments when available.

## GL comparison methodology

Normalize GL only when the rating basis is known and consistently measured. For example, if a quote is rated on gross sales, a screening ratio can be:

`annual GL premium / gross sales × 1,000`

Do not compare that ratio to a payroll-rated quote or compare quotes with materially different limits, exclusions, subcontractor treatment, project mix, claims context, or coverage forms. Prioritize standardized Albano quote/renewal observations over generic internet averages when sample size and data quality are sufficient.

## Quality controls before publication

- Store effective and expiration dates; never silently roll an old rate forward.
- Record source URL, source name, retrieval/review date, data type, and reviewer.
- Validate class code and wording against the current official classification.
- Flag missing data rather than filling gaps with a different trade's rate.
- Separate official references, carrier rates, quote-derived observations, and estimates in the UI.
- Keep client data private; do not commit identifiable policy or client records to this public repository.
- Display comparisons as below / within / above reference only when the exposure and coverage bases are sufficiently comparable. Treat results as review triggers, not proof of overpayment or guaranteed savings.
