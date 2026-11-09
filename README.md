# DEMETRA Dataset Portal

> Open dataset portal for the DEMETRA (Agriculture 4.0 — PNRR) project.  
> Hyperspectral & NIR leaf-level spectral data paired with laboratory nutrient assays.

**Live site:** `https://demetra-unime-cnr.github.io`

---

## Repository structure

```
demetra-dataset/
├── index.html          # Dataset portal (GitHub Pages entry point)
├── CITATION.cff        # Machine-readable citation metadata
├── LICENSE             # CC BY 4.0
├── README.md           # This file
└── datasets/
    └── .gitkeep        # Placeholder — actual data shipped via GitHub Releases
```

> **Note:** `.xlsx` files are **not** committed to the repository.  
> They are attached to [GitHub Releases](../../releases) to keep the repo lightweight.

---

## Partners

| Institution | Role |
|---|---|
| **University of Messina — Stratus Lab** | Lead institution — ML pipeline, band selection, dataset curation |
| **CNR-IEIIT** | Co-investigator — instrumentation, signal processing, acquisition protocols |

---

## Dataset releases

Each GitHub Release corresponds to a data version and contains the `.xlsx` files
listed on the portal. See [Releases](../../releases) for the full history.

| File | Campaign | Spectra | Bands |
|---|---|---|---|
| `wheat_spring_2023.xlsx` | Wheat — Spring 2023 | 312 | 2151 |
| `tomato_summer_2023.xlsx` | Tomato — Summer 2023 | 487 | 2151 |
| `vineyard_autumn_2023.xlsx` | Vineyard — Autumn 2023 | 258 | 2151 |
| `multicrop_spring_2024.xlsx` | Multi-crop — Spring 2024 | 701 | 2151 |

---

## Licence

Data and portal code © University of Messina — Stratus Lab & CNR-IEIIT.  
Released under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

**Citation is mandatory.** See `CITATION.cff` or the portal's "How to cite" section.

---

## How to deploy

### First-time setup

1. Fork or clone this repo under your GitHub organisation.
2. Go to **Settings → Pages**, set source to `main` branch, root `/`.
3. The portal will be live at `https://demetra-unime-cnr.github.io`.

### Adding datasets

1. Go to **Releases → Create a new release**.
2. Tag: `v1.0` (increment for updates: `v1.1`, `v2.0` …).
3. Drag & drop the `.xlsx` files as release assets.
4. Publish the release.
5. In `index.html`, update the `RELEASE_BASE` constant with the new version tag if needed:
   ```js
   const RELEASE_BASE = 'https://github.com/Demetra-UNIME-CNR/Demetra-UNIME-CNR.github.io/releases/download/v1.0/';
   ```

### Updating the citation

When the paper is published, edit the `#citationText` block in `index.html` and
update `CITATION.cff` with the final DOI, journal, and page numbers.

---

## Contact

For questions about the data: **stratus.lab@unime.it**
