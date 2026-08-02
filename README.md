# SG SME AI — evidence brief

By **Lobang Scout**.

**Live:** https://lobang-scout.github.io/sme-evidence/

Can Claude run a Singapore SME's back office? We stress-tested four setups against five synthetic
Singapore SMEs: plain Claude, Anthropic's `small-business` plugin, Claude plus MCP connectors, and
the accounting software SMEs already use.

~280 graded runs (Jun 2026), plus a July 2026 re-run on a newer model.

## What we found

- **The plugin's workflow text is written for the US and makes Singapore GST worse.** US receipt
  thresholds, a sales-tax model, and no GST or IRAS logic at all. Across 28 scored runs it added no
  quality over plain Claude, and it subtracted on statutory work.
- **We measured the damage: about S$6,400 of IRAS underpayment** in one run, from claiming import
  GST without a permit plus revenue drift.
- **A connector has no country.** An MCP connector is a generic API bridge. "Singapore-ness" comes
  from the connected account's configuration, not from the connector. An earlier draft of this brief
  got that wrong, and the correction is in the brief.
- **The real limit is the tool surface, not the country.** Even a Singapore-configured Xero
  organisation's MCP cannot file the GST F5, because statutory filing is not among the tools it
  exposes. That happens in the web product.
- **Roughly 3 of the 12 bundled connectors are a clean fit for Singapore.** Square does not operate
  here at all.

## Honesty notes

- **All business data is synthetic.** Five fabricated, PDPA-safe personas: a bubble tea chain, a
  minimart, an aircon servicing outfit, a design studio, a back-office bookkeeper.
- **Dated evidence, not advice.** Runs are from Jun to Jul 2026. Product capabilities and Singapore
  grant schemes change, and grant support is mid-transition through 2026. Verify current scheme
  terms at the source before budgeting. Nothing here is tax advice.
- **No ask.** Nothing to sign up for, no email capture, no gate. Read it, check the sources,
  disagree with it.
- Every external claim links to a primary source in the brief.

## Why this is no longer passphrase-gated (2026-08-03)

The gate protected synthetic data, and "contact the owner for the passphrase" is a request from an
account with no name, which is the shape phishing takes. A pseudonym earns trust by publishing
checkable work and asking for nothing, not by holding it back. The evaluation is the credibility;
hiding it defeated the point.
