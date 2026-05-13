# Contributing to Awesome HTML Slide Skills

Thanks for thinking about contributing! This list is curated, not crowd-sourced — but well-scoped PRs are very welcome.

## What we accept

A new entry must be:

1. **A real GitHub repository.** Public, accessible without auth, with working code committed (not just a README).
2. **Open-licensed.** MIT, Apache-2.0, BSD, CC-BY, MPL, GPL — anything OSI- or CC-approved. No "all rights reserved" or "personal use only" repos.
3. **HTML-output first.** The skill must produce HTML slides as the primary output, or the template repo must consist of HTML templates. PPTX export is fine *as an additional output* — but a pure PPTX skill (e.g. python-pptx with no HTML preview path) belongs in a different awesome list.
4. **About slides specifically.** General "make any frontend page" skills are out of scope unless they include a dedicated slide mode.
5. **Reasonably maintained.** Last commit within the past 18 months, or clear documentation that the project is "stable / done."

## What we reject (politely)

- Demos, gists, or single-file scripts without project structure.
- Repos that are just a fork of another listed project with no meaningful changes.
- Skills that are unsupported wrappers around a paid SaaS (the wrapper must do real work).
- Self-promotional listings that don't add a new style, workflow, or capability already covered by an existing entry.

## How to add an entry

1. Fork the repo and create a branch: `add/<repo-name>`.
2. Add your entry to **both** `README.md` and `README.zh-CN.md`. Match the existing format exactly — header level (`####`), star badge, blockquote tagline, body paragraphs, feature bullets. Use the latest star count from `https://api.github.com/repos/OWNER/NAME`.
3. Place the entry in the correct tier based on stars at PR-open time:
   - **Tier S** — 1,000 stars or more.
   - **Tier A** — 100 to 999 stars.
   - **Tier B** — under 100 stars.
4. Within a tier, entries are ordered by stars descending. Insert yours at the correct position.
5. Open the PR with a one-line description: *"Add `owner/repo` (XX stars) to Tier A."* Link to the repo and mention why it's not duplicative of existing entries.

## Updating star counts

Stars drift. A periodic refresh PR (re-querying every repo via the GitHub API and updating the badges) is welcome — open it with the title *"Refresh star counts (YYYY-MM-DD)"*. Don't change anything else in that kind of PR; keep it diffable.

## Reporting issues

- **Broken link / renamed repo** — open an issue with the old and new URLs.
- **License revoked / repo gone private** — open an issue; we'll remove the entry.
- **Project we missed** — open an issue with a link and a one-paragraph pitch; we'll triage and either invite a PR or add it ourselves.

## Style notes

- English README is the source of truth. When adding an entry, write the English version first, then mirror the structure in `README.zh-CN.md` with a faithful translation (don't paraphrase — the tier ordering and feature bullets must stay aligned across both files).
- Keep taglines as the project's own one-liner (often the GitHub description or README subtitle) — don't editorialize.
- Feature bullets can be lightly edited for consistency, but specific numbers (theme counts, layout counts, etc.) must match the project's actual claims.

## License of contributions

By submitting a PR, you agree that your changes are licensed under the same [CC BY 4.0](LICENSE) license that covers the curation work in this repo.
