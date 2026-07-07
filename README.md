# AJRI — American Journal of Research & Innovation

Standalone static website for the AJRI journal, published by Lifeline Emed Companies LLC.
Completely independent of the main Lifeline Emed site — no build step, no dependencies.

## Pages

| Page | File |
|---|---|
| Home | `index.html` |
| About AJRI | `about.html` |
| Aims & Scope | `aims-scope.html` |
| Peer Review | `peer-review.html` |
| Publication Ethics | `publication-ethics.html` |
| Author Guidelines | `author-guidelines.html` |
| Current Issue (Vol 1, Issue 1) | `current-issue.html` |
| Archives | `archives.html` |
| Submit Manuscript | `submit-manuscript.html` |
| Contact | `contact.html` |

Shared masthead nav + footer are injected by `assets/main.js`; all styling lives in `assets/styles.css`.

## Deploy to Vercel

From this folder:

```
npx vercel --prod
```

or push this folder to its own GitHub repo and import it in Vercel (no framework preset needed — it's plain static HTML).

## Connecting the Journal button on the main site

Once deployed (e.g. `https://ajri-journal.vercel.app`), edit the main site's `assets/main.js`:

- In `NAV_LINKS`, change the Journals entry to:
  `{ label: "Journals", href: "https://ajri-journal.vercel.app/" }`
- Update the two footer `journals.html` links the same way if desired.

The AJRI site already links back to the publisher site (`https://lifeline-emed-v4.vercel.app/`) in its footer and About page.
