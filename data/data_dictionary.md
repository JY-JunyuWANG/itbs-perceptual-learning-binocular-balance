# Data (CORTEX-S-26-00032)

This folder contains anonymized participant-level data files for the study:
**Sequence-dependent effects of iTBS and perceptual learning on binocular balance** (CORTEX-S-26-00032).

> Note: Participant identifiers are anonymized (e.g., `Sub001`). No direct identifying information is included.

## File naming convention

Example filename:

`Sub001_iTBS_PT_D1E1_LS-2024-11-20-16-41-SNR-0500`

### Components
- `Sub001`  
  Anonymized participant ID.  
  `Sub###` indicates the participant sequence number (e.g., `Sub001`, `Sub002`, ...).

- `D#` (Day index)  
  `D` denotes **Day** of experiment.  
  `D1–D3` correspond to Day 1 through Day 3.

- Session/block code (examples below)
  - `E` = **pre-test**  
    `E1–E2` correspond to pre-test Block 1 and Block 2 (e.g., `D1E1`, `D1E2`).
  - `L` = **perceptual training** during the intervention session  
    `L1–L6` correspond to training Block 1 through Block 6 (e.g., `D1L1` ... `D1L6`).
  - `O` = **post-test**  
    `O1–O2` correspond to post-test Block 1 and Block 2 (e.g., `D1O1`, `D1O2`).

- Protocol label in the intervention session: `LS` / `SL`
  - `LS` = **perceptual learning + iTBS**
  - `SL` = **iTBS + perceptual learning**

- Timestamp and recording parameters
  - Example: `2024-11-20-16-41`
  These fields reflect acquisition time.

## Data contents
- File format: MATLAB `.mat` (or archived as `.zip` containing `.mat` files).
- Each file corresponds to a specific participant (`Sub###`), day (`D#`), and block (`E/L/O` with block number).
- Primary outcomes and variable definitions should be documented in `data_dictionary.md`.

## Recommended usage
1. Download the data files (or the `.zip` archive, if provided) and extract them.
2. Use MATLAB to load `.mat` files, e.g.:
   ```matlab
   S = load('Sub001_iTBS_PT_D1E1_LS-2024-11-20-16-41-SNR-0500.mat');
   whos('-file','Sub001_iTBS_PT_D1E1_LS-2024-11-20-16-41-SNR-0500.mat');
