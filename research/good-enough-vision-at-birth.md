---
layout: page
title: Good-Enough Vision at Birth
permalink: /research/good-enough-vision-at-birth/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

Good-Enough Vision at Birth asks what face-relevant visual information remains under newborn-like visual degradation (rod-dominated, low-acuity input). This project uses computational models to test whether reduced visual input can still support meaningful face discrimination performance.

<div class="project-authors">Author: Yuexin Li<sup>1</sup></div>
<div class="project-affiliations"><sup>1</sup> New York University</div>

## Background

- Newborn infants have severely limited visual acuity and immature foveal cone systems.
- Even so, infants show early sensitivity to face-like patterns and structured visual input.
- This project tests whether early competencies may be supported by coarse rod-dominated signals rather than adult-like high-resolution vision.

## Research Questions

- How much visual structure remains under rod-weighted, low-acuity conditions?
- Is this reduced visual information sufficient for face-relevant discrimination tasks?
- Which signals remain robust vs. collapse under degradation?

## Methods and Modeling Pipeline

- Stimuli: schematic canonical/scrambled faces and real neutral faces (Chicago Face Database).
- Newborn-like visual simulation: grayscale normalization, `32 × 32` resize, Gaussian blur, optional Sobel edges.
- Tasks:
  - Schematic canonical vs. scrambled classification
  - Neutral Face vs. phase-scrambled classification
  - Attractiveness prediction/classification
  - Cross-orientation generalization tests
  - Model comparison focused on how well decodable signal survives degradation.

<div class="project-figure-grid">
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/preprocessing_pipeline_panel.png' | relative_url }}" alt="Preprocessing pipeline for newborn-like visual input simulation">
    <figcaption>Preprocessing pipeline used to simulate newborn-like visual input conditions before downstream modeling tasks.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/example_stimulus_panel.png' | relative_url }}" alt="Example stimuli panel for Good-Enough Vision at Birth">
    <figcaption>Example schematic and photographic stimuli under newborn-like degradation settings.</figcaption>
  </figure>
</div>

## Results Summary

- Canonical vs. scrambled schematic faces remained near-perfectly discriminable after newborn-like degradation.
- Real faces vs. phase-scrambled controls also remained near ceiling, including under center-cropping tests.
- Attractiveness classification stayed above chance under degraded input; best linear model reached about `0.74` accuracy.
- Cross-orientation generalization dropped from around `0.73–0.74` (within orientation) to around `0.46–0.48` (cross orientation), suggesting orientation-sensitive surviving signal.

## Result Figures

<div class="project-figure-grid">
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/main_performance_comparison.png' | relative_url }}" alt="Main task performance comparisons">
    <figcaption>Main task performance comparisons under newborn-like degraded input.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/cross_orientation_comparison.png' | relative_url }}" alt="Cross-orientation generalization comparison">
    <figcaption>Within-orientation versus cross-orientation generalization performance.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/crop_robustness_figure.png' | relative_url }}" alt="Crop robustness analysis figure">
    <figcaption>Crop-robustness checks for face-related discrimination performance.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/good-enough-vision-at-birth/attractiveness_interpretability_figure.png' | relative_url }}" alt="Attractiveness interpretability figure">
    <figcaption>Attractiveness-focused interpretability analyses under degraded input.</figcaption>
  </figure>
</div>

## Discussion

- Coarse degraded input can still support multiple face-related discriminations.
- This weakens the assumption that infant face sensitivity requires adult-like high-resolution input.
- These models are demonstrations of informational sufficiency, not full biological mechanism models.

## Limitations

- Retinal/input degradation is simplified relative to neonatal vision.
- No explicit modeling of eye movements, attention, or learning dynamics.
- Models act as ideal-observer demonstrations rather than process-level developmental accounts.

## Poster

Poster presented at 2026 Cognitive Development Society Meeting & 2026 NYU MA Psychology Research Conference.

- [View or download poster PDF]({{ '/docs/research/good-enough-vision-at-birth-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/good-enough-vision-at-birth-poster.pdf' | relative_url }}" title="Good-Enough Vision at Birth poster"></iframe>
</div>
