---
layout: page
title: Good-Enough Vision at Birth
permalink: /research/good-enough-vision-at-birth/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

**Good-Enough Vision at Birth** asks what kinds of face-relevant visual information remain usable under newborn-like visual degradation (rod-dominated, low-acuity input).
This project uses computational models to test whether reduced visual input can still support meaningful discrimination performance.

## Team and Context

- Author: Yuexin Li
- Department: Psychology, New York University
- Project type: Computational modeling

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
- `Schematic vs. scrambled` classification
- `Face vs. phase-scrambled` classification
- `Attractiveness` prediction/classification
- `Cross-orientation` generalization tests
- Model comparison focused on how well decodable signal survives degradation.

## Example Stimuli

<figure class="project-figure">
  <img src="{{ '/media/research/example_stimulus_panel.png' | relative_url }}" alt="Example stimuli panel for Good-Enough Vision at Birth">
  <figcaption>Example schematic and photographic stimuli under newborn-like degradation settings.</figcaption>
</figure>

## Results Summary

- Canonical vs. scrambled schematic faces remained near-perfectly discriminable after newborn-like degradation.
- Real faces vs. phase-scrambled controls also remained near ceiling, including under center-cropping tests.
- Attractiveness classification stayed above chance under degraded input; best linear model reached about `0.74` accuracy.
- Cross-orientation generalization dropped from around `0.73–0.74` (within orientation) to around `0.46–0.48` (cross orientation), suggesting orientation-sensitive surviving signal.

## Discussion

- Coarse degraded input can still support multiple face-related discriminations.
- This weakens the assumption that infant face sensitivity requires adult-like high-resolution input.
- These models are demonstrations of informational sufficiency, not full biological mechanism models.

## Limitations

- Retinal/input degradation is simplified relative to neonatal vision.
- No explicit modeling of eye movements, attention, or learning dynamics.
- Models act as ideal-observer demonstrations rather than process-level developmental accounts.

## Graphs and Assets (Where to Put Files)

Please place project graphics in:

- `/media/research/good-enough-vision-at-birth/`

Recommended filenames:

- `main-task-performance.png`
- `cross-orientation-generalization.png`
- `crop-robustness.png`
- `attractiveness-interpretability.png`

When you add them, I can drop them into the page immediately.

## Poster (Full)

- [View or download poster PDF]({{ '/docs/research/good-enough-vision-at-birth-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/good-enough-vision-at-birth-poster.pdf' | relative_url }}" title="Good-Enough Vision at Birth poster"></iframe>
</div>
