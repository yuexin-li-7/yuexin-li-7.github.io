---
layout: page
title: Eye-Track-ML
permalink: /research/eye-track-ml/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

Eye-Track-ML is a machine-learning pipeline for automated frame-by-frame coding of eye-tracking videos. The project integrates event classification, object detection, segmentation, and rule-based gaze mapping to reduce manual annotation burden while maintaining near-human accuracy.

<div class="project-authors">Authors: Mischa Gushiken<sup>1</sup>, Yuexin Li<sup>2</sup>, Jean Ee Tang<sup>1</sup>, Peter Gordon<sup>1</sup></div>
<div class="project-affiliations"><sup>1</sup> Teachers College, Columbia University<br><sup>2</sup> Columbia University</div>

## Background

- Eye-tracking supports attention and cognition research, but manual coding remains labor-intensive and sensitive to inter-coder variability.
- Large developmental datasets make fully manual frame-by-frame coding difficult to scale and reproduce.
- This project was motivated by an infant event representation dataset with `72` videos (more than `6` hours and over `600,000` frames), where automated support became essential.

## Research Question

- How can machine learning models be combined in a pipeline to automate fixation-point annotation in eye-tracking videos with minimal human intervention?

## Pipeline

- First: Break participant videos into individual frames.
- Second: Run YOLOv11 image classification to identify event type in each frame (for example, `hug-with-toy` vs. `hug-w/o-toy`).
- Third: For object detection, compare YOLO-only rectangular bounding boxes with YOLO+SAM2.1 contour-based segmentation masks.
- Fourth: Apply gaze-mapping rules to determine what participants are looking at when gaze indicators occlude objects, mapping abstract gaze coordinates to scene entities.
- Fifth: Consolidate outputs into participant CSV files.
- Human verification: Use a custom video overlay to validate and correct pipeline outputs frame by frame as needed.

## Experimental Validation

- Experiment 1: YOLO-only object detection against human-verified labels.
- Experiment 2: YOLO+SAM2.1 segmentation with mask-dilation comparison.
- Experiment 3: Symbolic verification for event classification outputs.
- Experiment 4: Overall pipeline reliability and agreement with human verification.

## Results Summary

- YOLO-only baseline reached `88.88%` overall accuracy.
- YOLO+SAM2.1 improved performance to `93.57%` with no dilation.
- `10px` dilation performed best at `94.24%`; performance declined beyond that range.
- Symbolic verification reached `99.18%` and then `100%` on event-classification checks.
- Combined SAM+YOLO (with `10px` dilation) outperformed YOLO-only by `5.36%`.

## Discussion

- A hybrid ML pipeline can automate large portions of frame-level eye-tracking annotation while preserving high accuracy.
- Segmentation-aware processing (YOLO+SAM2.1) materially improves fixation assignment over bounding-box-only baselines.
- Symbolic verification is a strong reliability layer for classification outputs.
- Human verification remains important for subtle edge cases, even with high automated performance.

## Poster

- [View or download poster PDF]({{ '/docs/research/eye-track-ml-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/eye-track-ml-poster.pdf' | relative_url }}" title="Eye-Track-ML poster"></iframe>
</div>
