# Copilot Cowork — ANZ Public Sector Use Case Navigator

An interactive, single-file web app that helps public servants across **Australia and New Zealand** discover, tailor, and copy **Microsoft Copilot Cowork** prompts for common government workflows. Pick a scenario, lock a jurisdiction profile, and generate a ready-to-use prompt with the relevant legislative and policy considerations automatically appended.

> **Planning aid only.** Confirm current legislation, policy, delegations, product capability, security, privacy, records, accessibility, workplace, and administrative-law requirements before implementation.

## Highlights

- **7 core scenarios** spanning information access, consultation, briefings, meetings, digests, reconciliation, and entity research.
- **17 workload patterns** — each scenario offers multiple task variants with their own inputs, outputs, and prompts.
- **11 jurisdiction profiles** — NZ Central, NZ Local, AU Commonwealth, NSW, Victoria, Queensland, Western Australia, South Australia, Tasmania, ACT, and Northern Territory.
- **Jurisdiction-aware prompts** — selecting a profile appends the correct access, privacy, records, engagement, finance, and meeting rules for that jurisdiction.
- **One-click copy** of the complete, tailored prompt.
- **Search and filter** by keyword, government function, risk level, and cadence.
- **Responsive design** — works on desktop, tablet, and mobile, with a collapsible filter panel on small screens.
- **Light/dark theme** — follows the OS preference automatically, or force it via a `?scoutTheme=dark` / `?scoutTheme=light` query parameter.
- **Zero dependencies** — a single self-contained HTML file with no build step, no network calls, and no tracking.

## Getting started

No installation or build is required.

1. Clone or download this repository.
2. Open `Copilot-Cowork-Public-Sector-Use-Cases-ANZ.html` in any modern browser.

To share it, host the single HTML file on any static web host (GitHub Pages, SharePoint, an internal file share, etc.).

### Optional: force a theme

Append a query parameter to the URL:

```
Copilot-Cowork-Public-Sector-Use-Cases-ANZ.html?scoutTheme=dark
Copilot-Cowork-Public-Sector-Use-Cases-ANZ.html?scoutTheme=light
```

## How to use

1. **Find a use case** — search or filter by government function, risk, or cadence. On mobile, tap **Filters** to expand the panel.
2. **Explore a scenario** — open a card to see what it does, its orchestrated flow, inputs, outputs, human-accountability model, and controls.
3. **Choose a workload** — switch between the task variants within a scenario.
4. **Lock a jurisdiction** — select a profile tab to append that jurisdiction's legislative and policy considerations to the prompt.
5. **Copy the prompt** — click **Copy prompt** and paste it into Copilot Cowork.

## Understanding risk levels

Each scenario carries a risk rating that reflects the sensitivity of the material, the consequences of relying on a flawed output, and how reversible the downstream decision is.

| Level | Meaning | Examples |
| --- | --- | --- |
| 🔴 **High** | Directly touches legal rights, privacy, or external release. | Information access, Public consultation, Entity research dossier |
| 🟡 **Medium** | Informs a formal decision or record, but a human certifies it. | Briefing/report/deck, Meeting lifecycle, Comparison and reconciliation |
| 🟢 **Low** | Internal, easily reversible convenience with no external release. | Priority and delivery digests |

## Shared design principles

- **Human accountability** — Cowork produces; authorised public servants verify, decide, approve, and release.
- **Jurisdiction lock** — one profile per run; never blend legal frameworks across jurisdictions.
- **Source integrity** — use only approved, version-controlled sources; log all access and transformations.
- **Proportionality** — apply only the domain rules relevant to the workload; do not over-configure.
- **Auditability** — retain generated artefacts, corrections, overrides, approvals, and incident records.
- **Continuous review** — review profiles whenever law, policy, templates, delegations, or product capability changes.

## Project structure

```
.
├── Copilot-Cowork-Public-Sector-Use-Cases-ANZ.html   # The complete app (HTML + CSS + JS + data)
└── README.md
```

All content — scenarios, workloads, jurisdiction rules, and design principles — lives in the `DATA` object inside the HTML file. Edit that object to add or update scenarios; the UI, stats, filters, and comparison tables render from it automatically.

## Browser support

Works in current versions of Edge, Chrome, Firefox, and Safari. Uses the native `<dialog>` element and the Clipboard API for the copy feature.

## Disclaimer

This catalogue is a planning aid to support discovery and design. It does not constitute legal, policy, or procurement advice, and does not replace an agency's own assessments. Always confirm current legislation, delegations, security, privacy, records, and accessibility requirements before deploying any workflow.

## License

Internal planning resource. Add a license here if this repository is to be shared publicly.
