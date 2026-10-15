# Contractor Insurance Risk Analysis — Albano Insurance Solutions

A static, browser-based MVP for reviewing contractor insurance premiums and flagging insurance-program issues for follow-up.

## Where it lives
- Launch page: `/`
- Diagnostic app: `/diagnostic/`
- App source: `diagnostic/index.html`

## Current MVP features
- Contractor profile, renewal, revenue/payroll, vehicles, and annual premiums by line
- WC premium per $100 payroll and GL premium per $1,000 revenue where inputs are available
- Optional comparison against user-entered benchmark rates
- Prioritized prompts for class-code/payroll, audit, subcontractor documentation, contract endorsement, certificate, loss-run, market strategy, and renewal reviews
- Print / Save PDF, JSON export, and copy-summary actions
- Responsive layout and Albano branding
- No backend and no form submission: entered intake data remains in the browser unless the user exports it

## Deploy with GitHub Pages
The repository's existing GitHub Actions workflow in `.github/workflows/static.yml` publishes repository contents on pushes to `main`. After this feature is merged to `main` and Pages is configured to use GitHub Actions, the launch page should be available at the repository's Pages URL and the diagnostic at the `/diagnostic/` path. Check the Actions tab for the deployment result; do not assume it is live until the workflow succeeds.

## Important limits
- This is a screening tool, not an insurance quote, coverage determination, underwriting decision, actuarial analysis, or guarantee of savings.
- Do not treat missing data as evidence of a problem.
- Only compare rates against a documented benchmark with matching state, trade/class, exposure basis, limits, and underwriting context.
- No validated third-party benchmark data is embedded.
- No sensitive personal information should be entered.
- Do not add API keys, CRM credentials, or customer information to this static public repository.

## Next recommended steps
1. Review the diagnostic UI and calculation assumptions with the agency.
2. Pilot with a small set of contractors and compare outputs against manual file reviews.
3. Add documented, approved benchmark sources and versioned methodology before presenting peer comparisons.
4. Only after the workflow and privacy requirements are approved, plan secure CRM integration through a server-side service.
