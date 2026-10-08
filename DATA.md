# DATA.md — datasets, versions, links, licenses

Fill this in during Week 2. Record exact versions — portals change.

| Dataset | Version / collection | Link | License | Used for |
|---|---|---|---|---|
| Sentinel-1 SAR GRD | `COPERNICUS/S1_GRD` via Google Earth Engine | https://earthengine.google.com | Free (Copernicus) | Main input, both areas, 2022-08-28–2022-09-12 |
| Sen1Floods11 hand-labeled | S1Hand + LabelHand + split CSVs | https://github.com/cloudtostreet/Sen1Floods11 | _check README_ | Global U-Net pretraining |
| JRC Global Surface Water | `JRC/GSW1_4`, occurrence > 90 | https://earthengine.google.com | Free | Permanent-water mask |
| District boundaries | HDX or GADM Pakistan | _paste link_ | _check_ | Flooded hectares per district |
| Copernicus EMS / UNOSAT | 2022 Pakistan activations | _paste links_ | Free | Visual reference only |
| Own labels | 45 tiles, CC BY 4.0 | this repo (`data/labels/`) | CC BY 4.0 | Fine-tune (Area A) + test (Area B) |

## Notes
- Sentinel-1 values in Earth Engine are already in dB (calibrated, terrain-corrected). Do NOT convert to dB again.
- Sen1Floods11 hand subset: check whether any chips are from Pakistan and disclose it in the report (areas/years differ, so the test stays valid).
- Study areas: Area A Sindh `[67.4, 26.4, 67.9, 26.9]` · Area B S. Punjab `[70.0, 28.8, 70.5, 29.3]` · EPSG:32642, 10 m.
