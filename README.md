# ATLAS AI — Opportunity Intelligence

ATLAS AI helps people discover educational, career, research and social-support opportunities, understand eligibility constraints, and turn leads into actionable plans.

**Status:** Public beta prototype (v0.1). No AI backend, live scraping, or automated applications yet. Demo opportunities are manually curated starting points. **No offer, deadline, eligibility or funding is guaranteed.**

## Try it

Open **[ATLAS AI](https://tilkitaha.github.io/ATLAS1/)** after GitHub Pages is enabled (Settings → Pages → Deploy from a branch → `main` / `(root)`).

Or clone and open `index.html` locally. No build step or API key required.

## Features

- Turkish/English interface
- Editable user profile (country, education, language, interests)
- Browse and search opportunities by category
- Explainable indicative matching — **not** an eligibility decision
- Save opportunities, organize an application action plan and export JSON
- Persistent browser localStorage; Reset Data option
- Accessibility: labels, keyboard-friendly controls, responsive layout

## Data integrity

Opportunity entries in `data/opportunities.js` link to primary official sources. Entries are illustrative discovery links, not verified open calls or vacancies. Consult the authoritative website for dates, requirements, residence rights and funding. The app never submits applications or transmits your profile to a server.

## Architecture

Static HTML + vanilla JS + CSS. Content stored locally in browser. `data/opportunities.js` serves as replaceable structured catalog.

```
index.html
assets/styles.css
assets/app.js
data/opportunities.js
.github/workflows/validate.yml
README.md
PRIVACY.md
LICENSE
```

## Development roadmap

1. Source ingestion from permitted official feeds/APIs with provenance and last-checked timestamps
2. Account system, secure storage, consent and data deletion
3. Explainable eligibility engine that separates hard rules from preference ranking
4. Applicant document parsing with explicit opt-in
5. Human-confirmed applications and deadline tracking
6. Multilingual accessibility testing, security review and verified opportunity coverage

## Run tests

```bash
node --check assets/app.js
node --check data/opportunities.js
python3 -m http.server 8080
```

Visit http://localhost:8080 . Node is only necessary for the syntax check.

## Contribute

Review suggestions and source corrections via GitHub issues. Never include confidential documents or personal information in a public issue.

## License

MIT. See [LICENSE](LICENSE).
