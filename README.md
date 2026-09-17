# Layered Insights GIS — Portfolio Viewer Demo

A working mockup of a property portfolio viewer built on GIS patterns
already proven internally: building footprints, floor plans, MEP contacts,
evacuation routes, and a maintenance/issue log. All data in this demo is
fictional — no real client, building, or vendor information.

This repo is intentionally separate from the main `layeredinsightsgis`
site repo, since this demo may grow its own backend (lead-capture gate,
issue-log storage) that shouldn't share a deploy pipeline with the core
marketing site.

## Status

Concept/demo stage. Not yet linked from the public site. See the private
`layeredinsightsgis_private/business/property-portfolio-viewer/` folder
for the strategy notes (concept, target market, tech stack decisions)
behind this build — nothing in that folder belongs here, and nothing here
should be copied there.

## Directory structure

```
layeredinsightsgis-portfolio-demo/
├── README.md         — this file
├── index.html        — the demo itself: single self-contained HTML/CSS/JS
│                        file, mock data for three fictional properties
│                        (office, multifamily, and a "pending survey"
│                        placeholder), no external dependencies beyond
│                        Google Fonts
└── worker/            — (not yet built) Cloudflare Worker source for the
                          email-gate lead-capture flow, if/when this demo
                          is exposed publicly on layeredinsightsgis.com.
                          Holds the KV read/write logic for captured
                          emails and issued access tokens. Do not build or
                          deploy this until the outside-activity approval
                          (case #2026-09-00000684) has cleared — see the
                          private repo's compliance notes.
```

## What's mock vs. real

Everything in `index.html` — building names, addresses, MEP contacts,
maintenance issues — is fictional, generated for demo purposes. Nothing
here is derived from UNG data, UNG infrastructure, or any real client.
