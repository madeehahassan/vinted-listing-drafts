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

Version 0.2.1 is packaged for public directory submission under the name **Vinted Listing Drafts**. It includes a primary icon, listing metadata, a support destination, a privacy note and a Claude Code marketplace entry. No public repository or directory submission has been confirmed yet. The package contains no seller photos, listings, credentials, browser state or telemetry. A full Claude agent run remains unverified because the local OAuth session expired during the portability test.

## Go-live review, 12 October 2026

1. Auth and user data: no plugin account, server, database or shared user store. Vinted transfer uses the seller's existing session only after item approval.
2. API security: no API keys, secrets, hidden network endpoints or bundled executable code. It instructs the host not to request credentials.
3. Cost controls: no paid service in the package. Host AI usage and any optional image tool costs depend on the seller's host account; the skill does not authorize charges.
4. Errors: missing facts stay flagged; unavailable browser control produces a manual handoff. Photos and listing claims require checks before transfer.
5. Performance: 11-photo local sample converted and loaded in the review page. No runtime application ships in the package.
6. Mobile: not applicable to this desktop photo-folder and browser workflow.
7. Legal and privacy: independent of Vinted, with a privacy note for the public repository. No license selected yet.
8. Production deploy: no server deployment. Directory review is separate from publishing and may reject the package.
9. Soft launch: local sample validated in Codex; a full Claude run still needs retesting after sign-in.

Verdict: ready with caveats for repository publication and directory review, not a claim of full cross-host validation.
