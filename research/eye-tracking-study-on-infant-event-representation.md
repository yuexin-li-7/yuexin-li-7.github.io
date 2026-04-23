---
layout: page
title: Eye-Tracking Study on Infant Event Representation
permalink: /research/eye-tracking-study-on-infant-event-representation/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

How Infant Looking Patterns to Trivalent Events Change from Object to Person Interaction asks whether pre-linguistic infants shift gaze-transition patterns with age in ways that reflect increasing event parsing and intention understanding.

- Authors: Mischa Gushiken, Yuexin Li, Peter Gordon

## Background

- Home-sign systems show that argument-structure-like conceptual organization can emerge without full linguistic input.
- Trivalent events such as `GIVE` and `SHOW` both involve three arguments, but differ in intentional complexity.
- This project tests whether infants parse these events differently across development.

## Research Questions

- Do gaze transition patterns change from 7 to 11 months, specifically away from `Toy↔Body` and toward `Face↔Face` transitions?
- Do `GIVE` and `SHOW` differ in the developmental trajectory of these gaze patterns?

## Methods and Modeling Pipeline

- Participants: 40 infants (7-11 months) and 15 adults in a within-subjects design.
- Event conditions: `GIVE` and `SHOW` (with multiple trial variants and quality-screened usable samples).
- Stimuli and coding:
  - Looped event videos
  - Eye-Track-ML pipeline for dynamic `Elements of Interest (EOIs)` detection and segmentation
  - Frame-by-frame extraction of transitions across face, toy, and body EOIs
- Statistical approach:
  - Gaussian GEE weighted by transition count
  - Linear age-trend tests across 7-11 months
  - Fixation threshold: `>=3` consecutive frames
  - Trial inclusion threshold: `>=50%` on-screen looking

<div class="project-figure-grid">
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-prior-work.png' | relative_url }}" alt="Prior work framing on event structure and argument representation">
    <figcaption>Conceptual and developmental framing for verb-argument structure and trivalent event parsing.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-eye-track-ml.png' | relative_url }}" alt="Eye-Track-ML pipeline and EOI coding example">
    <figcaption>Eye-Track-ML workflow and example segmented EOI output used for transition analysis.</figcaption>
  </figure>
</div>

## Results Summary

- In `GIVE`, `Face↔Face` transitions increased with age (`beta=0.053`, `p=.001`), while `Toy↔Body` transitions decreased (`beta=-0.078`, `p=.006`).
- In `SHOW`, `Face↔Face` transitions also increased (`beta=0.033`, `p=.007`), and `Toy↔Body` transitions decreased (`beta=-0.075`, `p<.0001`).
- Toy-to-face transitions showed a stronger age trend for `SHOW` than for `GIVE`.
- By 10-11 months, infants approached adult-like patterns for `GIVE` but remained less adult-like for `SHOW`.

## Result Figures

<div class="project-figure-grid">
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-give-condition.png' | relative_url }}" alt="GIVE condition age-trend plots">
    <figcaption>GIVE condition: age-related increases in face-oriented transitions and decreases in toy-body transitions.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-show-condition.png' | relative_url }}" alt="SHOW condition age-trend plots">
    <figcaption>SHOW condition: similar directional changes, but with slower convergence to adult-like transition patterns.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-give-vs-show-table.png' | relative_url }}" alt="GIVE versus SHOW comparison table">
    <figcaption>Summary of linear age trends across transition types in GIVE and SHOW conditions.</figcaption>
  </figure>
</div>

## Discussion

- Results support a developmental shift from object/body-centered transitions toward face-centered transitions.
- This shift is stronger and earlier for `GIVE` than for `SHOW`, consistent with greater conceptual complexity for SHOW-type intentional relations.
- The findings align with prior work suggesting physical transfer relations may be parsed before deeper intention-driven structures.

## Limitations

- Correlational developmental trends cannot fully isolate mechanism.
- EOI segmentation quality and trial inclusion thresholds may influence effect size estimates.
- Additional longitudinal/replication datasets will help test robustness across populations and task variants.

## Poster

Poster presented at 2026 Cognitive Development Society Meeting.

- [View or download poster PDF]({{ '/docs/research/eye-tracking-study-on-infant-event-representation-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/eye-tracking-study-on-infant-event-representation-poster.pdf' | relative_url }}" title="Eye-Tracking Study on Infant Event Representation poster"></iframe>
</div>
