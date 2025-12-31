# Literature Review: Narrative Manipulation Analysis on Video
### Course Assignment 1

**Student:** Andrii Hupalo  
**Date:** December 31, 2025

---

## 📂 Repository Contents

### 1. `CA1_Hupalo_Andrii.pdf`
- The final technical report formatted in Springer LNCS style.

### 2. `CA1_Hupalo_Latex.zip`
- Complete LaTeX source code package.
- **Includes:**
  - `samplepaper.tex`: The main source code.
  - `saturation.png`: The terminology saturation analysis graph (Figure 2 in the report).
  - `sampling_methods.png`: Methodology diagram (Figure 1 in the report).
  - `llncs.cls`: Springer class file required for compilation.

### 3. `data/` (Research Evidence)
This folder contains the raw artifacts from the "Controlled Snowball Sampling" pipeline:

- **`011_exported.xlsx`**: The bibliography (N=29) selected on step 11.
- **`007_restricted_snowball_output.jsonl`**: The complete list of **1,228 relevant papers** identified by the algorithm (validating the N=1,228 statistic in the report).
- **`008_search_path_count_output.jsonl`**: Intermediate log calculating the "Main Path" history of the field.
- **`in-seed.csv`**: The 9 initial seed papers used to start the search.
- **`config.ini`**: The configuration parameters used for the search.

---

## ⚙️ Methodology & Technical Note

The literature search was conducted using a **Controlled Snowball Sampling** Python pipeline.

### Data Collection Statistics
- **Total Candidates Processed:** 20,587
- **Relevant Corpus Identified:** 1,228 (See `data/007_restricted_snowball_output.jsonl`)
- **Final Selection:** ~30 papers (See `data/011_exported.xlsx`). It included not only papers but books alos. Was adjusted.

### Pipeline Execution
1.  **Seed Selection:** 9 initial papers.
2.  **Expansion:** API calls to OpenAlex/Semantic Scholar.
3.  **Filtering:** Restricted Snowball (SSNMF Topic Modeling).
4.  **Validation:** Terminology Saturation Analysis (included in `CA1_Hupalo_Latex.zip`).
