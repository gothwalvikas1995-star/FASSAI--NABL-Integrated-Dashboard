# NABL Integrated Labs — Regulator Dashboard

Interactive dashboard of NABL-accredited laboratories with regulator recognition (FSSAI, EIC, APEDA, Tea Board, Spices Board, IOPEPC, CDB, SHEFEXIL): India map with state/district drill-down, scope filters, cross-regulator recognition view and clickable KPIs.

**Single static file** — `index.html` contains all code and data, no build step.

## Demo accounts (prototype only)

The login screen lists the demo accounts; select one to fill the form.

| Profile | Email | Sees |
|---|---|---|
| Admin | admin@nabl.test | all labs |
| FSSAI, EIC, APEDA, Tea Board, Spices Board, IOPEPC, CDB, SHEFEXIL | `<regulator>@nabl.test` (e.g. `fssai@nabl.test`) | only the labs that regulator recognises |

The sign-in check runs in the browser, so this is a demo and not a security boundary: all lab data is in the page source.

## Hosting

- **GitHub Pages:** serves `index.html` from the `main` branch root.
- **Vercel:** import this repository in Vercel (framework preset "Other", no build command, output directory = repository root), or use the one-click link:
  https://vercel.com/new/clone?repository-url=https://github.com/gothwalvikas1995-star/FASSAI--NABL-Integrated-Dashboard
