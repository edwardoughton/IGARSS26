# IGARSS 2026 Summer School
## AI Refusnik to AI Evangelist: Excelling at AI-Assisted Coding for Satellite Image Analysis

**Instructor:** Ed Oughton, George Mason University

**Event:** IEEE International Geoscience and Remote Sensing Symposium (IGARSS) 2026 Summer School

**Session length:** 2–3 hours (three ~50-minute parts)

**Audience:** First and second year PhD students with some Python experience

---

## Overview

This session takes participants on a practical journey from satellite image data acquisition through
to AI-assisted processing pipelines.

The title reflects a real journey many researchers take (including myself), for example, from initial scepticism about AI coding
tools to becoming a productive, critical user who understands both the power and the risks.

Importantly, it is imperative that students (i) exercise their critical thinking skills while developing AI-assisted code and interpreting results, and (ii) essential that all outputs are tested and validated (as code will always be garbage in, garbage out). 

---

## Notebooks

* Notebook 1
* Notebook 2
  
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
