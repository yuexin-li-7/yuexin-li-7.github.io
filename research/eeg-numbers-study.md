---
layout: page
title: Electroencephalogram (EEG) Numbers Study
permalink: /research/eeg-numbers-study/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

Electrophysiological and Behavioral Indices of Numerical Perception and Cognition examines how set size and change direction shape behavioral performance and EEG responses during numerical-change detection.

<div class="project-authors">Authors: Jean Ee Tang<sup>1</sup>, Yuexin Li<sup>2</sup>, Paul Smith<sup>1</sup>, Janiece Spitzmueller<sup>1</sup>, Mischa (Yuri) Gushiken<sup>1</sup>, Christofer Tobing<sup>1</sup>, Peter Gordon<sup>1</sup></div>
<div class="project-affiliations"><sup>1</sup> Teachers College, Columbia University<br><sup>2</sup> Columbia University</div>

## Background

- Prior work on numerical cognition supports two processing systems: a small-number/subitizing system and a large-number approximation system.
- EEG studies have linked numerical processing to parietal-occipital-temporal (`POT`) responses, especially N1-related effects.
- This project tests whether those neural patterns also capture directional and categorical differences within a tighter numerical range.

## Research Questions

- Do behavioral accuracy and reaction time vary by numerical-change set size (`SS`, `SL/LS`, `LL`) and change direction (increasing vs. decreasing)?
- Do N1 and P3b components show systematic amplitude/latency differences across these change conditions?
- Do ERP effects support a categorical distinction between small- and large-number processing?

## Procedure and EEG Processing

- Participants: `24` right-handed adults (ages `23–43`, mean `27.7`) completed a numerical-change detection task.
- EEG acquisition: `128`-channel EGI Geodesic Sensor Net with high-impedance amplifier; recordings sampled at `250 Hz`, with electrode impedance kept below `50 kΩ`.
- ERP windows:
  - N1: `125–200 ms`
  - P3b: `435–535 ms`
- Processing workflow:
  - `0.1–100 Hz` recording band with `40 Hz` low-pass digital filtering for analysis
  - `800 ms` epochs with `100 ms` pre-stimulus baseline
  - Artifact rejection, re-referencing, and condition-wise averaging within participants

## Experimental Conditions and Statistical Plan

- Change set-size conditions: within small (`SS`), within large (`LL`), and crossover (`SL/LS`).
- Change direction conditions: increasing (for example, `1→2`, `5→6`) versus decreasing (for example, `5→4`, `3→2`).
- Numerical change distance tested at differences of `1`, `2`, and `3`.
- Analyses included repeated-measures ANOVA, ERP condition contrasts, and correlation analyses linking EEG indices with behavior.

## Results Summary

- Behavioral effects:
  - Accuracy showed significant effects of set size (`p<0.0001`) and direction (`p<0.01`).
  - Reaction time showed significant effects of set size (`p<0.0001`), direction (`p<0.01`), and their interaction (`p<0.0001`).
  - Accuracy was lowest for `LL`, and reaction time was longest for increasing-large changes.
- ERP effects:
  - N1 and P3b profiles varied across direction and set-size combinations.
  - In `SS` and crossover sets, decreasing changes elicited stronger N1/P3b responses; trends were reversed in `LL` sets.
- Brain-behavior coupling:
  - P3b latency correlated with reaction time (`r=0.425`, `p<0.01`).
  - N1 and P3b amplitudes showed positive correlation (`r=0.263`, `p<0.05`).

## Discussion

- Findings support a neural distinction between small and large numerical processing during change detection.
- N1 responses scaled with cardinal value in the small-number range (`1–3`) but not in the large range (`4–6`).
- P3b patterns align with context-updating and working-memory accounts of change detection.
- Relative to prior wide-gap designs, this narrower `1–6` continuum still revealed category-like transitions in both behavior and ERPs.

## Poster

- [View or download poster PDF]({{ '/docs/research/eeg-numbers-study-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/eeg-numbers-study-poster.pdf' | relative_url }}" title="Electroencephalogram (EEG) Numbers Study poster"></iframe>
</div>
