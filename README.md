# SG SME AI: the evidence brief

By **Lobang Scout**. Working out AI, together.

**Live:** https://lobang-scout.github.io/sme-evidence/

Can Claude run a Singapore SME's back office? I stress-tested four setups against five synthetic
Singapore businesses: plain Claude, Anthropic's `small-business` plugin, Claude plus MCP
connectors, and the accounting software SMEs already use.

About 280 graded runs in June 2026, plus a July 2026 re-run of the safety rounds on a newer model.

## The headline is that the headline moved

**In June, an unguarded model underpaid GST badly on a naive close.** It claimed import GST off
overseas invoices with no Customs permit, in 40% of plain runs and 60% of runs with the plugin. The
worst one was out by about S$9,200.

**In July, on a newer model, that failure was gone. Zero times in thirteen runs.** The model closed
the gap by itself, so the June headline is no longer true.

**The behavioural failures did not close.** Unguarded, it still promised a customer a refund the
owner never approved, eight drafts out of eight. The plugin still invented cash-flow confidence
bands in all four runs. A short set of Singapore guardrails cut both to zero out of four.

Knowledge gaps shrink with each model release. Behavioural gaps do not. Do not buy a tool for
something the next model will do anyway; buy guardrails for behaviour and connectors for reach.

## What else it found

- **The plugin's workflow text is written for the US and made Singapore GST worse.** US receipt
  thresholds, a sales-tax model, and no GST or IRAS logic at all. Across 28 scored runs it added
  no quality over plain Claude, and it subtracted on statutory work. On the newer model the tax
  harm has faded; the fabricated confidence bands have not.
- **A connector has no country.** An MCP connector is a generic API bridge. "Singapore-ness" comes
  from the connected account's configuration, not from the connector. An earlier draft of this
  brief got that wrong, and the correction is in the brief with the original claim still visible.
- **The real limit is the tool surface, not the country.** Even a Singapore-configured Xero
  organisation's MCP cannot file the GST F5, because statutory filing is not among the tools it
  exposes. That happens in the web product.
- **Roughly 3 of the 12 bundled connectors are a clean fit here.** Square does not operate in
  Singapore at all.

## Honesty notes

- **All business data is synthetic.** Five fabricated, PDPA-safe personas: a bubble tea chain, a
  minimart, an aircon servicing outfit, a design studio, a back-office bookkeeper.
- **The re-run was small.** Four to thirteen runs per cell. Directional, not conclusive, and worth
  widening to more trades and to a field test on a real consented SME's live Xero.
- **Everything was written by Claude Sonnet and graded by Claude Opus**, never the same model
  marking its own work.
- **Dated evidence, not advice.** Runs are from June and July 2026. Product capabilities and
  Singapore grant schemes change, and grant support is mid-transition through 2026. Check current
  scheme terms at the source before you budget anything. Nothing here is tax advice.
- **No ask.** Nothing to sign up for, no email capture, no gate. Read it, check the sources,
  disagree with it.
- Every external claim links to a primary source in the brief.

## Why this is no longer passphrase-gated (2026-08-03)

The gate protected synthetic data, and "contact the owner for the passphrase" is a request from an
account with no name, which is the shape phishing takes. A pseudonym earns trust by publishing
checkable work and asking for nothing, not by holding it back. The evaluation is the credibility;
hiding it defeated the point.
