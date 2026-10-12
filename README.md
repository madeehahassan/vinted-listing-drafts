# Vinted Listing Drafts

This is an independent plugin by Madeeha Hassan. It is not affiliated with Vinted.

It contains two skills. `prepare-listings` turns a photo folder into checked JPEGs and editable, researched listing records. `submit-approved-listings` transfers only the items the seller has approved to Vinted. The package contains instructions and a record format; it does not contain a hosted listing desk, photo-editing service, Vinted API integration or seller data. The agent needs access to the seller's local photos and web research. Transfer also needs authorized browser control and a Vinted session where the seller is already signed in.

## Install

Claude Code users can run `claude plugin marketplace add madeehahassan/vinted-listing-drafts` and then `claude plugin install vinted-listing-drafts@madeeha-plugins`.

For Codex, install the ZIP from this repository's Releases page through the desktop plugin interface. The root `plugin.json` is the portable Agent Plugins manifest; `.codex-plugin/plugin.json` is the Codex compatibility manifest.

## Try locally

- Claude Code: run `claude plugin validate ./vinted-listing-plugin`, then `claude --plugin-dir ./vinted-listing-plugin`. Invoke `/vinted-listing-drafts:prepare-listings` with the photo folder. After review, invoke `/vinted-listing-drafts:submit-approved-listings` and name the approved items.
- Codex: install the package through the desktop plugin interface, then start a new chat and ask for Vinted Listing Drafts on a named folder.

The seller chooses country, currency, language and pricing preferences. Originals remain unchanged. Research links and uncertainty flags stay with each listing. No Vinted upload happens during preparation.

For help, open an issue in this repository. See [the privacy note](PRIVACY.md) for what stays on the seller's computer and what reaches Vinted when the seller approves a transfer.

The plugin is packaged for directory review. It does not include any seller photos, listings, credentials or browser data. Directory approval and public availability depend on each platform's review.
