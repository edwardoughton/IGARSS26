# IGARSS 2026 Summer School
## AI Refusnik to AI Evangelist: Excellent at AI-Assisted Coding for Satellite Image Analysis

**Instructor:** Ed Oughton, George Mason University

**Event:** IEEE International Geoscience and Remote Sensing Symposium (IGARSS) 2026 Summer School

**Session length:** 2–3 hours (three ~50-minute parts)

**Audience:** First and second year PhD students with some Python experience

---

## Overview

This session takes participants on a practical journey from satellite image data acquisition through
to AI-assisted processing pipelines, with a rigorous focus on testing and validation at the end.

The title reflects a real journey many researchers take (including myself), for example, from initial scepticism about AI coding
tools to becoming a productive, critical user who understands both the power and the risks.

Importantly, it is imperative that students (i) exercise their critical thinking skills while developing AI-assisted code and interpreting results, and (ii) essential that all outputs are tested and validated (as code will always be garbage in, garbage out). 

### We have a three-part structure for the afternoon

| Part | Topic | Duration |
|---|---|---|
| **Part 1** | Landsat & Sentinel-2 data download and processing | ~60 min |
| **Part 2** | AI agents for data processing pipeline construction | ~60 min |
| **Part 3** | Testing, validation, and uncertainty quantification | ~60 min |

---

## Notebooks

### Part 1 — Satellite Image Data Acquisition

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/edwardoughton/IGARSS26/blob/main/notebook_1_data_acquisition.ipynb)

**`notebook_1_data_acquisition.ipynb`**

Covers:
- Connecting to the Microsoft Planetary Computer STAC API
- Searching and downloading **Landsat Collection 2 Level 2** surface reflectance data
- Searching and downloading **Sentinel-2 Level 2A** surface reflectance data
- Computing spectral indices: NDVI, NDWI, NDBI
- Visualizing true-colour and false-colour composites
- Saving analysis-ready GeoTIFF outputs
- Comparing Landsat (30 m) and Sentinel-2 (10 m) spatial resolution

---

### Part 2 — AI Agents for Data Processing

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/edwardoughton/IGARSS26/blob/main/notebook_2_ai_agents.ipynb)

**`notebook_2_ai_agents.ipynb`**

Covers:
- The AI Refusnik → AI Evangelist mindset shift
- Prompt engineering: the **CAPE framework** (Context, Action, Parameters, Expected output)
- Setting up an OpenAI-compatible AI agent in Python
- Using AI to generate a **K-Means unsupervised land cover classification** pipeline
- Using AI to generate an **NDVI change detection** workflow
- Critically evaluating AI-generated geospatial code
- Common AI code failure modes and how to catch them

---

### Part 3 — Testing, Validation and Uncertainty

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/edwardoughton/IGARSS26/blob/main/notebook_3_testing_validation.ipynb)

**`notebook_3_testing_validation.ipynb`**

Covers:
- Why testing is especially important when using AI-generated code
- Writing `pytest` unit tests for remote sensing processing functions
- Building synthetic test fixtures with known spectral properties
- Computing a full **accuracy assessment**: confusion matrix, overall accuracy, Cohen's Kappa
- **Monte Carlo uncertainty propagation** for spectral indices
- Generating a reproducibility report for AI-assisted pipelines
- End-to-end integration tests

---

## Prerequisites

Participants should be comfortable with:
- Python basics (variables, functions, loops)
- `numpy` array operations
- Running Jupyter Notebooks (or Google Colab)

No prior remote sensing programming experience is assumed — all concepts are introduced from scratch.

---

## Running the notebooks

### Option A: Google Colab (recommended — no local setup required)

Click the **Open In Colab** badge above each notebook. All dependencies are installed in the first cell.

### Option B: Local environment

```bash
pip install pystac-client planetary-computer odc-stac rasterio numpy matplotlib \
            scikit-learn scipy geopandas shapely openai pytest ipytest
jupyter lab
```

---

## Acknowledgements

These materials build on content originally developed for GGS 416 Satellite Image Analysis
at George Mason University:
https://github.com/edwardoughton/satellite-image-analysis

The preparation of these open-source materials has been gratefully supported by research
funding from NASA Cooperative Agreement 80NSSC25M0077.
