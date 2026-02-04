# Multi-Tone Signal Filtering (100 Hz, 200 Hz, 300 Hz, 400 Hz)

##  Project Overview
This task focuses on designing suitable filters to isolate specific frequency components from a composite input signal made of multiple sine waves.

The input signal is:

\[
x(t) = A_1\sin(2\pi \cdot 100t) + A_2\sin(2\pi \cdot 200t) + A_3\sin(2\pi \cdot 300t) + A_4\sin(2\pi \cdot 400t)
\]

Where:
- \(A_1, A_2, A_3, A_4\) are amplitudes  
- The frequencies present are: **100 Hz, 200 Hz, 300 Hz, 400 Hz**

---

##  Objective
Design appropriate filters to isolate different frequency components using one of the following filter types:

- **Low Pass Filter (LPF)**
- **High Pass Filter (HPF)**
- **Band Pass Filter (BPF)**
- **Band Stop Filter (BSF / Notch)**

Each filter must include correct cutoff frequency/frequencies.

---

##  Design Strategy
To cleanly separate the tones, cutoff frequencies are selected at the **midpoints between adjacent frequencies**:

- Between **100 Hz and 200 Hz → 150 Hz**
- Between **200 Hz and 300 Hz → 250 Hz**
- Between **300 Hz and 400 Hz → 350 Hz**

These midpoints act as natural boundaries for filter cutoff values.

---

## Filter Design Table

| Frequency Component to Isolate | Filter Type | Cutoff Frequency/Frequencies |
|---|---|---|
| **100 Hz** | Low Pass Filter (LPF) | fc = **150 Hz** |
| **400 Hz** | High Pass Filter (HPF) | fc = **350 Hz** |
| **100 Hz and 200 Hz** | Low Pass Filter (LPF) | fc = **250 Hz** |
| **200 Hz** | Band Pass Filter (BPF) | **150 Hz – 250 Hz** |
| **300 Hz** | Band Pass Filter (BPF) | **250 Hz – 350 Hz** |
| **300 Hz and 400 Hz** | High Pass Filter (HPF) | fc = **250 Hz** |
| **200 Hz and 300 Hz** | Band Pass Filter (BPF) | **150 Hz – 350 Hz** |
| **200 Hz, 300 Hz, and 400 Hz** | High Pass Filter (HPF) | fc = **150 Hz** |
| **100 Hz and 400 Hz** | Band Stop Filter (BSF) | Stopband: **150 Hz – 350 Hz** |

---


---

## Example Use Cases
- Extracting the **100 Hz** component → LPF (150 Hz)
- Extracting only **200 Hz** → BPF (150–250 Hz)
- Extracting **300 Hz and 400 Hz** → HPF (250 Hz)
- Keeping only **100 Hz and 400 Hz** (remove middle tones) → BSF (150–350 Hz)

---


