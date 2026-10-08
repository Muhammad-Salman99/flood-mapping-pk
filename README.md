# Flood Extent Mapping of Pakistan from Sentinel-1 SAR Imagery Using Deep Learning

Research prototype — not an official product. Do not use for emergency decisions.

## Team
- Muhammad Salman (lead)
- Ismat Khalil
- Muhammad Bilal
- Husnulmab Saeed

UET Peshawar, CS & IT · Oct–Nov 2026

## What this is
Detects flood water in Sentinel-1 SAR imagery for two study areas in Pakistan (2022 floods):
- **Area A** — Sindh, Dadu/Manchar Lake region (training + fine-tuning)
- **Area B** — Southern Punjab, Rajanpur region (final test only, never touched during training)

Three methods are compared on the held-out Area B: Otsu thresholding (baseline),
U-Net trained on Sen1Floods11 (global), and U-Net fine-tuned on Area A labels.

## Repo layout
```
notebooks/   01_export_gee … 07_district_areas (run in order)
data/        NOT committed (too large) — raw GeoTIFFs, tiles, labels, districts live in Drive
splits/      areaA_train.txt, areaA_val.txt, areaB_test.txt (frozen lists)
checkpoints/ NOT committed — model .pt files live in Drive, linked here
outputs/     figures/, maps/, district_flood_area.csv (small files committed)
report/      report source, slides
app.py       Streamlit dashboard (Week 6)
```

## Quickstart
1. Clone the repo and create a Python 3.10+ environment.
2. `pip install -r requirements.txt`
3. Data lives in the shared Google Drive folder (link below) — copy `data/` next to the repo.
4. Run notebooks in order. Checkpoints are saved to Drive every epoch.

## Data
See `DATA.md` for dataset names, versions, links, and licenses.
Shared Drive folder: _(paste link here)_

## Results
_(results table goes here after Week 5)_

## License
Code: MIT. Own labels: CC BY 4.0. Third-party datasets are linked, not redistributed.
