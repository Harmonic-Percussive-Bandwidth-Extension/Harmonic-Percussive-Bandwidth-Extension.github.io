---
title: "Full Results"
layout: single
permalink: /results
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
excerpt: "Complete objective metrics"
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
---

This page gives the complete objective results for the paper, including the SI-SDR and waveform L1 values that the paper does not report. Why these two metrics are left out of the paper is explained in the first section below, [Why SI-SDR and waveform L1 are not used to compare systems](#why-si-sdr-and-waveform-l1-are-not-used-to-compare-systems).

Unless stated otherwise, values are means over the MUSDB18 test set (n = 1000, 25 s excerpts), with 95 % pivotal bootstrap confidence intervals in brackets, truncated to two decimals. Waveform L1 is in units of 10⁻².

## Why SI-SDR and waveform L1 are not used to compare systems

The "do-nothing" anchor (the band-limited input simply upsampled to 48 kHz, which performs no bandwidth extension at all) obtains the *best* SI-SDR (22.47 dB) and the best waveform L1 (0.98·10⁻²) of any entry in Table A, and its SI-SDR is higher than HP-codecX's on every one of the 1000 test files. Both metrics are dominated by the 0–8 kHz band that every system receives unchanged as input, so they reward leaving the signal untouched rather than extending it. For this reason the paper compares systems with Mel distance, STFT distance and ViSQOL only. SI-SDR and waveform L1 are kept on this page for completeness and for comparison with prior work that reports them.

## Table A — Objective bandwidth extension metrics (paper Table IV)

MUSDB18 test set. Apollo and A2SB are scored at 44.1 kHz; the anchor, AudioSR, UniverSR and HP-codecX at 48 kHz.

| System | Mel ↓ | STFT ↓ | Waveform ↓ (10⁻²) | SI-SDR ↑ | ViSQOL ↑ |
|---|---|---|---|---|---|
| Anchor (band-limited input, no extension) | 2.13 [2.10, 2.16] | 6.16 [6.09, 6.23] | **0.9** [0.9, 1.0] | **22.47** [22.03, 22.88] | 1.92 [1.89, 1.94] |
| Apollo | 0.84 [0.83, 0.85] | 2.44 [2.41, 2.47] | 4.8 [4.8, 4.9] | 3.23 [3.00, 3.47] | 3.23 [3.20, 3.27] |
| AudioSR | 1.77 [1.74, 1.80] | 3.60 [3.55, 3.64] | 6.9 [6.8, 7.0] | 13.75 [13.44, 14.05] | 3.06 [3.03, 3.08] |
| A2SB | 0.63 [0.62, 0.64] | 2.65 [2.61, 2.69] | 1.2 [1.2, 1.3] | 19.70 [19.36, 20.04] | 3.08 [3.05, 3.11] |
| UniverSR | 1.32 [1.29, 1.34] | 3.53 [3.48, 3.58] | 0.9 [0.9, 1.0] | 22.38 [21.94, 22.80] | 2.28 [2.25, 2.31] |
| **HP-codecX** | **0.45** [0.44, 0.46] | **1.89** [1.87, 1.91] | 1.2 [1.2, 1.3] | 20.23 [19.78, 20.66] | **3.33** [3.31, 3.36] |

Bold marks the best value in each column, the anchor included. On waveform L1 the anchor (0.980·10⁻²) is ahead of UniverSR (0.986·10⁻²) by a margin smaller than either confidence interval.

Full-precision anchor values: Mel 2.134309 [2.108947, 2.160497]; STFT 6.162785 [6.095153, 6.231618]; waveform 0.009797 [0.009418, 0.010177]; SI-SDR 22.470424 [22.030500, 22.885937]; ViSQOL 1.924759 [1.897724, 1.949673].

## Table B — Ablation study (paper Table V)

Design choices: **ST** = structure-informed training, **MT** = multi-transformer prediction, **MR** = multi-RVQ, **FB** = frequency branches.

| Config | ST | MT | MR | FB | Mel ↓ | STFT ↓ | Waveform ↓ (10⁻²) | SI-SDR ↑ | ViSQOL ↑ |
|---|---|---|---|---|---|---|---|---|---|
| **HP-codecX** | ✓ | ✓ | ✓ | ✓ | **0.45** [0.44, 0.46] | **1.89** [1.87, 1.91] | 1.2 [1.2, 1.3] | **20.23** [19.78, 20.66] | **3.33** [3.31, 3.36] |
| EXP 1 | ✗ | ✓ | ✓ | ✓ | 0.48 [0.47, 0.48] | 1.97 [1.92, 1.99] | 1.2 [1.1, 1.2] | 20.03 [19.59, 20.44] | 3.08 [3.05, 3.10] |
| EXP 2 | ✗ | ✗ | ✓ | ✓ | 0.48 [0.47, 0.48] | 1.97 [1.95, 1.99] | 1.2 [1.1, 1.2] | 20.00 [19.57, 20.41] | 3.07 [3.04, 3.09] |
| EXP 3 | ✗ | ✗ | ✗ | ✓ | 0.84 [0.83, 0.85] | 2.83 [2.80, 2.86] | 2.4 [2.3, 2.5] | 14.63 [14.17, 15.08] | 2.48 [2.45, 2.51] |
| EXP 4 | ✓ | ✗ | ✗ | ✓ | 0.58 [0.57, 0.59] | 2.24 [2.21, 2.27] | 1.5 [1.4, 1.6] | 18.58 [18.14, 19.01] | 2.56 [2.53, 2.59] |
| EXP 5 | ✗ | ✗ | ✗ | ✗ | 1.06 [1.05, 1.07] | 2.81 [2.79, 2.84] | 5.7 [5.6, 5.8] | 6.68 [6.51, 6.85] | 3.14 [3.11, 3.17] |

Each configuration differs from the previous one by a single component, so consecutive rows isolate one design choice: HP-codecX→EXP 1 isolates structure-informed training, EXP 1→EXP 2 the multi-transformer, EXP 2→EXP 3 the multi-RVQ, EXP 3→EXP 5 the frequency branches. EXP 4 sits outside this chain, reintroducing structure-informed training on top of EXP 3. EXP 5 uses a standard 48 kHz DAC fed with upsampled audio. EXP 1 and EXP 2 are indistinguishable on every metric: the multi-transformer shows no measurable effect on its own.

### Model capacity of the ablation configurations

Parameters are counted twice: those the forward pass actually uses at inference, and those stored in the released checkpoints. Transformer passes are forward passes of a transformer stack per generated excerpt.

| Config | Params used at inference (M) | Params stored (M) | Transformer passes |
|---|---|---|---|
| HP-codecX | 247.9 | 347.3 | 6 (2 stacks × 3) |
| EXP 1 | 247.9 | 347.3 | 6 (2 stacks × 3) |
| EXP 2 | 172.3 | 259.1 | 6 (1 stack × 6) |
| EXP 3 | 173.4 | 260.2 | 6 (1 stack × 6) |
| EXP 4 | 173.4 | 260.2 | 6 (1 stack × 6) |
| EXP 5 | 194.1 | 194.1 | 12 (1 stack × 12) |

- **Structure-informed training (HP-codecX vs EXP 1)** is capacity-matched: the two configurations are identical in size.
- **Multi-RVQ (EXP 2 vs EXP 3) and structure-informed training without multi-RVQ (EXP 3 vs EXP 4)** are capacity-matched too: EXP 2, EXP 3 and EXP 4 differ by less than 1 %.
- **Multi-transformer (EXP 1 vs EXP 2)** is *not* capacity-matched: the second transformer stack gives EXP 1 44 % more parameters than EXP 2, at the same number of forward passes.
- **Frequency branches (EXP 3 vs EXP 5)** is the least comparable pair. EXP 5 has 22 % fewer parameters than HP-codecX but performs twice as many transformer passes, because its single stack predicts twelve codebooks instead of six.

All configurations use twelve codebooks of 1024 entries in the codec, so the codec bitrate is 12.0 kbit/s throughout, except EXP 5 at 11.25 kbit/s (93.75 instead of 100 frames per second).

## Table C — Per-section results across datasets (paper Table VI)

HP-codecX output reconstructed from the estimated harmonic tokens only (**H**), the estimated percussive tokens only (**P**), or both (**H+P**). Dataset families: *solo instruments* (Medley-solos-DB, OrchideaSOL), *harmonic* (Monophonic, Polyphonic), *percussive* (ENST-drums), *environmental sounds* (ESC-50), *speech* (VCTK).

**Silent clips.** Eight of the 1000 ESC-50 test excerpts (samples 144, 336, 765, 793, 836, 842, 936 and 996) are digital silence. SI-SDR is undefined on a silent reference (0/0, or the metric's −80 dB floor when the output is not exactly silent), and the spectral errors on silence measure only how much noise a system adds. All ESC-50 values on this page, in this table and in the out-of-domain tables below, are therefore computed on the remaining 992 excerpts.

### Mel ↓

| | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| H | 0.42 [0.41, 0.43] | 0.40 [0.39, 0.41] | 0.41 [0.39, 0.42] | 0.51 [0.50, 0.52] | 0.45 [0.44, 0.46] | 0.49 [0.46, 0.51] | 0.74 [0.73, 0.75] |
| P | 0.41 [0.40, 0.42] | 0.39 [0.38, 0.40] | 0.44 [0.43, 0.46] | 0.53 [0.52, 0.53] | 0.42 [0.41, 0.43] | 0.47 [0.45, 0.49] | 0.67 [0.66, 0.67] |
| H+P | 0.39 [0.39, 0.40] | 0.38 [0.37, 0.39] | 0.42 [0.41, 0.44] | 0.51 [0.50, 0.52] | 0.41 [0.40, 0.42] | 0.46 [0.44, 0.48] | 0.70 [0.69, 0.70] |

### STFT ↓

| | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| H | 1.71 [1.69, 1.74] | 1.87 [1.83, 1.91] | 3.52 [3.47, 3.58] | 3.56 [3.53, 3.59] | 1.74 [1.71, 1.77] | 2.08 [2.02, 2.13] | 2.91 [2.89, 2.93] |
| P | 1.71 [1.69, 1.74] | 1.84 [1.80, 1.88] | 3.68 [3.63, 3.73] | 3.73 [3.70, 3.76] | 1.66 [1.64, 1.69] | 2.07 [2.02, 2.13] | 2.73 [2.71, 2.75] |
| H+P | 1.67 [1.65, 1.70] | 1.81 [1.77, 1.86] | 3.63 [3.58, 3.68] | 3.66 [3.63, 3.69] | 1.63 [1.60, 1.66] | 2.04 [1.98, 2.10] | 2.79 [2.77, 2.81] |

### Waveform ↓ (10⁻²)

| | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| H | 0.3 [0.2, 0.3] | 0.3 [0.3, 0.3] | 0.08 [0.07, 0.08] | 0.2 [0.2, 0.2] | 0.7 [0.6, 0.7] | 1.0 [0.9, 1.1] | 0.5 [0.4, 0.5] |
| P | 0.3 [0.2, 0.3] | 0.3 [0.3, 0.3] | 0.07 [0.07, 0.08] | 0.2 [0.2, 0.2] | 0.7 [0.6, 0.7] | 1.0 [0.9, 1.1] | 0.5 [0.5, 0.5] |
| H+P | 0.3 [0.2, 0.3] | 0.3 [0.2, 0.3] | 0.07 [0.07, 0.08] | 0.2 [0.2, 0.2] | 0.7 [0.6, 0.7] | 1.0 [0.9, 1.1] | 0.5 [0.5, 0.5] |

### SI-SDR ↑

| | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| H | 37.47 [36.76, 38.16] | 35.31 [34.53, 36.10] | 43.85 [43.00, 44.69] | 28.87 [28.67, 29.06] | 18.91 [18.09, 19.74] | 20.70 [19.94, 21.46] | 21.29 [20.94, 21.64] |
| P | 37.21 [36.51, 37.89] | 35.50 [34.72, 36.28] | 43.83 [43.05, 44.61] | 29.14 [28.95, 29.33] | 18.53 [17.72, 19.35] | 20.32 [19.57, 21.09] | 20.35 [20.00, 20.70] |
| H+P | 37.59 [36.88, 38.30] | 35.90 [35.09, 36.69] | 44.18 [43.38, 45.00] | 29.17 [28.98, 29.36] | 18.82 [17.97, 19.64] | 20.67 [19.90, 21.44] | 20.86 [20.50, 21.21] |

### ViSQOL ↑

| | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| H | 3.04 [2.99, 3.09] | 3.07 [3.02, 3.13] | 4.14 [4.09, 4.18] | 3.65 [3.62, 3.67] | 3.26 [3.21, 3.31] | 2.93 [2.88, 2.98] | 2.45 [2.43, 2.47] |
| P | 3.09 [3.04, 3.14] | 3.08 [3.03, 3.14] | 4.14 [4.10, 4.18] | 3.76 [3.73, 3.78] | 3.33 [3.28, 3.38] | 3.02 [2.98, 3.07] | 2.50 [2.48, 2.52] |
| H+P | 3.21 [3.15, 3.26] | 3.18 [3.12, 3.23] | 4.20 [4.16, 4.24] | 3.80 [3.77, 3.82] | 3.40 [3.34, 3.45] | 3.12 [3.08, 3.17] | 2.50 [2.48, 2.52] |

## Table D — Codec reconstruction metrics (paper Table I)

MUSDB18 test set. soft-dis-DAC is the model of Giniès et al. with the harmonic and percussive RVQ sections removed; DAC is retrained on our dataset.

### 16 kHz

| Model | Mel ↓ | STFT ↓ | Waveform ↓ (10⁻²) | SI-SDR ↑ | ViSQOL ↑ |
|---|---|---|---|---|---|
| HP-codec | 0.79 [0.78, 0.79] | 2.26 [2.25, 2.28] | 4.8 [4.8, 4.9] | 7.23 [7.0, 7.4] | 4.34 [4.33, 4.34] |
| soft-dis-DAC | **0.70** [0.69, 0.70] | **2.11** [2.10, 2.13] | **4.1** [4.1, 4.2] | **8.75** [8.57, 8.93] | **4.43** [4.42, 4.43] |
| DAC | 0.82 [0.81, 0.82] | 2.32 [2.30, 2.34] | 5.1 [5.0, 5.2] | 6.80 [6.60, 6.99] | 4.37 [4.37, 4.38] |

### 48 kHz

| Model | Mel ↓ | STFT ↓ | Waveform ↓ (10⁻²) | SI-SDR ↑ | ViSQOL ↑ |
|---|---|---|---|---|---|
| HP-codec | 0.77 [0.77, 0.78] | 2.26 [2.25, 2.28] | 5.0 [4.9, 5.1] | 6.75 [6.59, 6.92] | **4.36** [4.35, 4.37] |
| soft-dis-DAC | **0.72** [0.72, 0.73] | **2.22** [2.20, 2.23] | 4.3 [4.2, 4.4] | 8.10 [7.92, 8.28] | 4.33 [4.32, 4.34] |
| DAC | 0.75 [0.75, 0.76] | 2.24 [2.22, 2.26] | **4.1** [4.0, 4.2] | **8.79** [8.61, 8.97] | 3.92 [3.90, 3.94] |

## Table E — Inference complexity (paper Table VII)

One NVIDIA L40S, 10 s mono excerpt, median of 10 runs after 3 warm-ups, IQR below 1 % of the median for every model. Params: evaluated at inference / stored in the checkpoints. NFE: network evaluations. RTF: processing time divided by signal duration.

| Model | Params (M) used / stored | NFE | RTF ↓ | Output rate |
|---|---|---|---|---|
| Apollo | 16.5 / 16.5 | 1 | 0.021 | 44.1 kHz |
| AudioSR | 762.0 / 1285.4 | 100 (+ HiFi-GAN vocoder) | 0.453 | 48 kHz |
| UniverSR | 57.0 / 57.0 | 16 | 0.431 | 48 kHz |
| A2SB | 565.5 / 1131.1 | 49 (× 6 windows for a 10 s input) | 2.974 | 44.1 kHz |
| HP-codecX | 247.9 / 347.3 | 6 (+ 1 encoder, 1 decoder) | 0.021 | 48 kHz |

HP-codec alone: 149.03 M parameters (16 kHz branch 73.88 M, 48 kHz branch 75.15 M; encoders 43.24 M, decoders 105.48 M, quantizers 0.307 M). HP-codecX transformers: 198.25 M stored, 173.06 M used at inference, 83.97 M per module. The second transformer adds 75.58 M parameters and no additional forward passes.

HP-codecX's lean inference path measures an RTF of 0.011; the figure in the table (0.021) is that of the released sample-generation script, which performs additional codec passes whose outputs are discarded.

## Supplementary data

### Harmonic/percussive energy concentration (paper Table III)

Change in energy concentration, in percent, between a reconstruction using only one RVQ section and the full reconstruction.

| | 16 kHz, H output | 16 kHz, P output | 48 kHz, H output | 48 kHz, P output |
|---|---|---|---|---|
| Harmonic energy | +12.6 | −41.1 | +25.3 | −37.5 |
| Percussive energy | −15.4 | +10.2 | −36.1 | +42.8 |

Harmonic energy concentrates in the harmonic reconstruction and percussive energy in the percussive reconstruction, at both sampling rates.

### HP-codec reconstruction by input type and RVQ section (paper Table II)

*Input* is the signal fed to HP-codec and used as the reference: the full mixture (Global), or its HPSS harmonic or percussive component. *Sections* are the RVQ sections used for decoding. MUSDB18 test set, n = 1000 per row.

| Input | Sections | Rate | Mel ↓ | STFT ↓ | Waveform (×10⁻²) ↓ | SI-SDR (dB) ↑ | ViSQOL ↑ |
|---|---|---|---|---|---|---|---|
| Global | H+P | 16 kHz | 0.79 [0.78, 0.79] | 2.26 [2.25, 2.28] | 4.88 [4.79, 4.97] | 7.23 [7.07, 7.40] | 4.34 [4.33, 4.34] |
| Global | H+P | 48 kHz | 0.77 [0.77, 0.78] | 2.26 [2.25, 2.28] | 5.01 [4.92, 5.11] | 6.75 [6.59, 6.91] | 4.36 [4.35, 4.37] |
| Global | H | 16 kHz | 1.06 [1.05, 1.06] | 2.64 [2.62, 2.66] | 6.04 [5.93, 6.14] | 5.07 [4.91, 5.23] | 4.06 [4.05, 4.07] |
| Global | H | 48 kHz | 0.93 [0.93, 0.94] | 2.49 [2.47, 2.51] | 6.12 [6.01, 6.22] | 4.75 [4.59, 4.90] | 4.22 [4.21, 4.23] |
| Global | P | 16 kHz | 1.06 [1.05, 1.07] | 2.69 [2.66, 2.71] | 6.68 [6.57, 6.78] | 3.84 [3.69, 3.99] | 4.17 [4.16, 4.18] |
| Global | P | 48 kHz | 0.94 [0.94, 0.95] | 2.49 [2.47, 2.51] | 6.74 [6.63, 6.85] | 3.52 [3.37, 3.67] | 4.24 [4.23, 4.26] |
| Harmonic | H+P | 16 kHz | 0.94 [0.93, 0.95] | 1.89 [1.87, 1.91] | 1.66 [1.62, 1.69] | 10.89 [10.73, 11.06] | 4.33 [4.32, 4.33] |
| Harmonic | H+P | 48 kHz | 1.56 [1.52, 1.60] | 2.24 [2.20, 2.27] | 3.94 [3.83, 4.04] | 3.62 [3.43, 3.80] | 3.92 [3.90, 3.93] |
| Harmonic | H | 16 kHz | 1.02 [1.01, 1.03] | 1.96 [1.95, 1.98] | 2.07 [2.03, 2.11] | 8.78 [8.62, 8.93] | 4.22 [4.21, 4.23] |
| Harmonic | H | 48 kHz | 1.62 [1.58, 1.65] | 2.31 [2.28, 2.34] | 4.05 [3.94, 4.15] | 2.96 [2.78, 3.14] | 3.84 [3.83, 3.86] |
| Harmonic | P | 16 kHz | 1.43 [1.41, 1.45] | 2.38 [2.35, 2.41] | 2.63 [2.57, 2.69] | 6.41 [6.23, 6.59] | 4.15 [4.14, 4.16] |
| Harmonic | P | 48 kHz | 1.60 [1.56, 1.63] | 2.25 [2.22, 2.28] | 4.23 [4.12, 4.33] | 1.77 [1.59, 1.96] | 3.86 [3.85, 3.88] |
| Percussive | H+P | 16 kHz | 1.66 [1.61, 1.71] | 2.47 [2.42, 2.52] | 2.61 [2.50, 2.70] | 4.80 [4.59, 5.02] | 4.28 [4.27, 4.28] |
| Percussive | H+P | 48 kHz | 1.32 [1.31, 1.34] | 1.87 [1.86, 1.89] | 1.49 [1.45, 1.53] | -3.78 [-4.00, -3.57] | 3.77 [3.75, 3.79] |
| Percussive | H | 16 kHz | 1.74 [1.69, 1.77] | 2.53 [2.49, 2.57] | 2.94 [2.84, 3.03] | 2.78 [2.58, 3.00] | 4.07 [4.06, 4.08] |
| Percussive | H | 48 kHz | 1.41 [1.39, 1.42] | 1.99 [1.98, 2.00] | 1.65 [1.60, 1.70] | -5.51 [-5.74, -5.28] | 3.71 [3.69, 3.73] |
| Percussive | P | 16 kHz | 1.81 [1.76, 1.85] | 2.60 [2.54, 2.64] | 2.89 [2.79, 2.98] | 2.56 [2.35, 2.77] | 4.23 [4.22, 4.23] |
| Percussive | P | 48 kHz | 1.28 [1.27, 1.29] | 1.86 [1.85, 1.87] | 1.56 [1.52, 1.61] | -4.69 [-4.91, -4.47] | 3.86 [3.84, 3.88] |

### Out-of-domain bandwidth extension (paper Fig. 5)

The values behind the out-of-domain heatmap, for all five metrics (the paper's figure shows Mel, STFT and ViSQOL). n = 1000 per cell. ESC-50 values are computed on 992 clips (see the note on silent clips under Table C).

#### Mel ↓

| System | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| Apollo | 1.02 [1.01, 1.04] | 1.09 [1.06, 1.11] | 0.61 [0.58, 0.64] | 1.06 [1.03, 1.08] | 1.03 [1.01, 1.05] | 0.95 [0.93, 0.98] | 0.99 [0.98, 1.00] |
| AudioSR | 1.21 [1.18, 1.23] | 1.10 [1.06, 1.14] | 1.06 [1.02, 1.10] | 0.88 [0.86, 0.90] | 1.38 [1.34, 1.41] | 1.39 [1.36, 1.42] | 1.49 [1.48, 1.51] |
| A2SB | 0.55 [0.54, 0.57] | 0.75 [0.72, 0.77] | 1.09 [1.03, 1.16] | 0.78 [0.77, 0.79] | 0.80 [0.78, 0.83] | 0.69 [0.66, 0.72] | 0.93 [0.92, 0.94] |
| UniverSR | 0.71 [0.69, 0.73] | 0.82 [0.80, 0.85] | 0.31 [0.30, 0.33] | 0.70 [0.68, 0.71] | 1.15 [1.12, 1.19] | 1.13 [1.09, 1.17] | 0.75 [0.74, 0.76] |
| **HP-codecX** | 0.39 [0.39, 0.40] | 0.38 [0.37, 0.39] | 0.42 [0.41, 0.44] | 0.51 [0.50, 0.52] | 0.41 [0.40, 0.42] | 0.46 [0.44, 0.48] | 0.70 [0.69, 0.70] |

#### STFT ↓

| System | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| Apollo | 2.73 [2.69, 2.76] | 2.87 [2.83, 2.91] | 2.38 [2.36, 2.40] | 2.60 [2.59, 2.61] | 2.59 [2.55, 2.63] | 2.81 [2.76, 2.86] | 2.35 [2.33, 2.36] |
| AudioSR | 2.76 [2.71, 2.81] | 2.54 [2.48, 2.60] | 3.04 [2.94, 3.14] | 2.64 [2.59, 2.69] | 2.45 [2.40, 2.50] | 3.14 [3.07, 3.21] | 2.89 [2.85, 2.92] |
| A2SB | 2.35 [2.29, 2.41] | 2.92 [2.87, 2.98] | 2.19 [2.11, 2.28] | 2.05 [2.02, 2.08] | 3.42 [3.35, 3.49] | 2.86 [2.79, 2.92] | 4.11 [4.08, 4.14] |
| UniverSR | 2.17 [2.13, 2.21] | 2.64 [2.59, 2.69] | 3.17 [3.11, 3.23] | 3.08 [3.04, 3.12] | 3.08 [3.01, 3.16] | 3.23 [3.16, 3.30] | 2.42 [2.38, 2.45] |
| **HP-codecX** | 1.67 [1.65, 1.70] | 1.81 [1.77, 1.85] | 3.63 [3.58, 3.68] | 3.66 [3.63, 3.69] | 1.63 [1.60, 1.66] | 2.04 [1.98, 2.10] | 2.79 [2.77, 2.81] |

#### Waveform ↓ (10⁻²)

| System | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| Apollo | 3.58 [3.47, 3.68] | 2.65 [2.52, 2.77] | 0.53 [0.48, 0.58] | 0.60 [0.56, 0.63] | 1.88 [1.75, 2.00] | 2.75 [2.60, 2.89] | 1.43 [1.36, 1.49] |
| AudioSR | 3.71 [3.60, 3.82] | 3.47 [3.30, 3.63] | 1.53 [1.46, 1.61] | 2.31 [2.25, 2.38] | 2.55 [2.43, 2.67] | 3.45 [3.29, 3.60] | 3.41 [3.34, 3.48] |
| A2SB | 0.42 [0.37, 0.46] | 0.38 [0.35, 0.42] | 0.37 [0.35, 0.39] | 0.47 [0.46, 0.48] | 0.77 [0.72, 0.82] | 1.20 [1.10, 1.29] | 0.56 [0.53, 0.58] |
| UniverSR | 0.27 [0.24, 0.31] | 0.27 [0.23, 0.30] | 0.05 [0.05, 0.06] | 0.18 [0.17, 0.18] | 0.69 [0.64, 0.74] | 0.98 [0.88, 1.06] | 0.47 [0.45, 0.49] |
| **HP-codecX** | 0.30 [0.26, 0.33] | 0.33 [0.29, 0.36] | 0.07 [0.06, 0.07] | 0.22 [0.21, 0.23] | 0.71 [0.66, 0.76] | 1.03 [0.94, 1.12] | 0.52 [0.50, 0.54] |

#### SI-SDR ↑

| System | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| Apollo | 5.75 [5.18, 6.33] | 12.48 [11.73, 13.23] | 30.42 [29.99, 30.84] | 26.27 [26.02, 26.53] | 8.60 [7.83, 9.38] | 8.41 [7.80, 9.03] | 15.87 [15.30, 16.44] |
| AudioSR | 22.28 [21.90, 22.67] | 22.55 [21.91, 23.17] | 25.06 [24.76, 25.36] | 20.11 [19.86, 20.36] | 12.49 [11.78, 13.17] | 13.18 [12.58, 13.81] | 13.83 [13.53, 14.13] |
| A2SB | 31.72 [31.23, 32.21] | 30.66 [30.02, 31.33] | 24.66 [23.98, 25.36] | 22.62 [22.38, 22.87] | 18.46 [17.74, 19.17] | 18.42 [17.74, 19.12] | 20.28 [19.95, 20.62] |
| UniverSR | 39.05 [38.35, 39.76] | 37.27 [36.49, 38.07] | 44.82 [44.07, 45.58] | 30.58 [30.37, 30.80] | 20.69 [19.87, 21.51] | 22.59 [21.82, 23.37] | 22.67 [22.32, 23.02] |
| **HP-codecX** | 37.59 [36.89, 38.30] | 35.90 [35.10, 36.69] | 44.18 [43.36, 44.98] | 29.17 [28.98, 29.36] | 18.82 [18.00, 19.63] | 20.67 [19.90, 21.44] | 20.86 [20.51, 21.22] |

#### ViSQOL ↑

| System | Medley-solos-DB | OrchideaSOL | Monophonic | Polyphonic | ENST-drums | ESC-50 | VCTK |
|---|---|---|---|---|---|---|---|
| Apollo | 2.94 [2.88, 2.98] | 2.71 [2.65, 2.78] | 4.20 [4.16, 4.25] | 2.97 [2.92, 3.01] | 2.96 [2.90, 3.02] | 2.84 [2.79, 2.89] | 2.51 [2.48, 2.53] |
| AudioSR | 2.90 [2.85, 2.95] | 2.92 [2.86, 2.98] | 3.38 [3.32, 3.44] | 2.98 [2.94, 3.02] | 3.28 [3.23, 3.33] | 2.90 [2.85, 2.96] | 2.78 [2.76, 2.81] |
| A2SB | 3.17 [3.12, 3.22] | 2.79 [2.73, 2.85] | 3.62 [3.57, 3.66] | 3.10 [3.06, 3.14] | 2.96 [2.90, 3.02] | 2.96 [2.91, 3.01] | 2.09 [2.06, 2.11] |
| UniverSR | 2.98 [2.93, 3.03] | 2.77 [2.70, 2.83] | 4.24 [4.19, 4.28] | 2.99 [2.94, 3.03] | 2.56 [2.50, 2.62] | 2.50 [2.45, 2.56] | 2.56 [2.54, 2.58] |
| **HP-codecX** | 3.21 [3.16, 3.26] | 3.18 [3.12, 3.23] | 4.20 [4.16, 4.24] | 3.80 [3.77, 3.82] | 3.40 [3.34, 3.45] | 3.12 [3.08, 3.17] | 2.50 [2.48, 2.52] |

## Listening test (paper Fig. 4)

MUSHRA, 13 listeners, 12 trials, 5 stimuli per trial, continuous 0–100 scale. Excerpts drawn from the MUSDB18 test set, six with high high-frequency energy and six from the remainder. Median and quartiles over all ratings.

| Stimulus | Median | Q1 | Q3 |
|---|---|---|---|
| Reference | 100 | 100 | 100 |
| HP-codecX | 86 | 75 | 100 |
| A2SB | 85.5 | 73 | 100 |
| Apollo | 65 | 50.75 | 79.25 |
| Anchor (low-pass) | 51.5 | 32 | 65.25 |

Tests on per-listener means: a Friedman test shows a significant effect of condition (χ²(4) = 49.05, p < 10⁻⁹). Holm-corrected Wilcoxon signed-rank tests find HP-codecX rated higher than Apollo and the anchor by all 13 listeners (p<sub>Holm</sub> < 0.001), with no significant difference from A2SB (p<sub>Holm</sub> = 0.38); a TOST establishes equivalence of HP-codecX and A2SB within ±10 MUSHRA points (p < 0.001).
