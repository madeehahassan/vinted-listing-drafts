# Vinted Listing Drafts public package spec

## Purpose

Give a private seller a portable, local-first workflow for turning product photos into researched, editable Vinted listings and transferring only explicitly approved items.

## Package

One plugin with two skills: preparation and approved transfer. Include the portable Agent Plugins manifest and compatibility manifests for Claude Code and Codex. Keep the record format inside the preparation skill. Include no seller photos, listings, browser state, credentials, personal review desk URL or machine-specific path.

## Required behaviour

Inventory every source file; group photos by product; preserve originals; convert working copies to checked JPEGs; reject inaccurate photo edits; research product and price matches using direct links; keep price evidence types separate; create editable records and review flags; show selected JPEGs in listing order with JPEG filenames; keep unverified condition blank; verify discard, restore and edit persistence; distinguish draft approval from publication approval; verify Vinted results after transfer.

## Local portability test

On 12 October 2026, an isolated UK/GBP test used 11 copied HEIC photos covering three pairs. All 11 converted to full-size JPEGs, and a local review page grouped the pairs, showed comparison links, and flagged unknown condition and size. A browser check confirmed all images loaded and price edits, discard and restore survived refresh. Claude Code loaded the plugin package, but a live Claude run stopped before reading photos because its local OAuth session had expired. The preparation workflow was executed manually by Codex; a full Claude agent run remains unverified.

## Distribution status

Version 0.2.2 is published in a public GitHub repository under the name **Vinted Listing Drafts**. It includes a primary icon, listing metadata, support and privacy links, and a Claude Code marketplace entry. A clean Claude configuration installed version 0.2.1 from that public marketplace successfully; 0.2.2 adds repository metadata and publication status. Claude directory-only manifest fields are held until this machine's Claude CLI supports them without validation warnings. No official directory submission has been confirmed. The package contains no seller photos, listings, credentials, browser state or telemetry. A full Claude agent run remains unverified because the local OAuth session expired during the portability test.

## Go-live review, 12 October 2026

1. Auth and user data: no plugin account, server, database or shared user store. Vinted transfer uses the seller's existing session only after item approval.
2. API security: no API keys, secrets, hidden network endpoints or bundled executable code. It instructs the host not to request credentials.
3. Cost controls: no paid service in the package. Host AI usage and any optional image tool costs depend on the seller's host account; the skill does not authorize charges.
4. Errors: missing facts stay flagged; unavailable browser control produces a manual handoff. Photos and listing claims require checks before transfer.
5. Performance: 11-photo local sample converted and loaded in the review page. No runtime application ships in the package.
6. Mobile: not applicable to this desktop photo-folder and browser workflow.
7. Legal and privacy: independent of Vinted, with a privacy note for the public repository. No license selected yet.
8. Production deploy: no server deployment. The public GitHub marketplace is live. Anthropic's current directory portal requires a paid Claude plan; this account shows Free. OpenAI's plugin dashboard requires developer identity verification and a valid default payment method before upload. Neither official directory submission is complete.
9. Soft launch: local sample validated in Codex; a full Claude run still needs retesting after sign-in.

Verdict: ready with caveats for repository publication and directory review, not a claim of full cross-host validation.
