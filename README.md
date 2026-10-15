# Albano Contractor Insurance Risk Analysis

**Insurance Optimization Made Easy**

A browser-based MVP for reviewing contractor insurance premiums and flagging issues for follow-up.

## Launch the tool
- **Diagnostic app:** [Open the Contractor Insurance Diagnostic](./diagnostic/)
- **Launch page:** [Open the project landing page](./)
- **Benchmark table:** [California contractor WC and GL cost references](./benchmarks.html)

## Current features
- Intake for contractor trade, renewal, revenue, payroll, vehicles, and annual premiums by coverage line
- Workers' compensation premium per $100 payroll and general liability premium per $1,000 revenue calculations when inputs are available
- Optional user-entered benchmark comparisons with clear comparability caveats
- Prioritized prompts for class codes, audit readiness, subcontractor documentation, contract endorsements, certificates, loss runs, renewal planning, and market strategy
- Print / Save PDF, JSON export, and copy-summary actions
- Sourced benchmark reference page: California WCIRB advisory pure premium rates effective September 1, 2026, plus clearly labeled GL premium-to-revenue estimates converted to cost per $1,000
- Responsive design with Albano Insurance Solutions branding

## Privacy and limitations
This is a static browser-only tool. The form does not submit customer information to a server; data remains in the browser unless the user exports it. Do not enter sensitive personal information.

This MVP is a preliminary screening aid, not an insurance quote, underwriting decision, coverage opinion, actuarial analysis, validated peer benchmark, or guarantee of savings. Benchmark rates should be used only when the state, trade/class, exposure basis, limits, and underwriting context are comparable. No validated external benchmark dataset is included.

## GitHub Pages
The existing GitHub Actions workflow in `.github/workflows/static.yml` deploys repository contents on pushes to `main`. Confirm the workflow succeeds in the [Actions tab](https://github.com/cgibson2432/contractor-scorecard/actions) before relying on the live Pages URL.

## Next steps
1. Review the output and calculations with the agency.
2. Pilot against manual reviews for a small group of contractors.
3. Add documented benchmark sources and a versioned methodology before presenting peer comparisons.
4. Design secure server-side CRM integration only after data handling and workflow requirements are approved.

Albano Insurance Solutions · 916-864-4983 · CA License 0D16140 · Agency License 0442296
