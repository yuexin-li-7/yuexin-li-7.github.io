---
layout: page
title: Eye-Tracking Study on Infant Event Representation
permalink: /research/eye-tracking-study-on-infant-event-representation/
---

[Back to Research]({{ '/research/' | relative_url }})

## Project Overview

How Infant Looking Patterns to Trivalent Events Change from Object to Person Interaction asks whether pre-linguistic infants shift gaze-transition patterns with age in ways that reflect increasing event parsing and intention understanding.

<div class="project-authors">Authors: Mischa Gushiken<sup>1</sup>, Yuexin Li<sup>2</sup>, Peter Gordon<sup>1</sup></div>
<div class="project-affiliations"><sup>1</sup> Teachers College, Columbia University<br><sup>2</sup> New York University</div>

## Background

- Home-sign systems show that argument-structure-like conceptual organization can emerge without full linguistic input.
- Trivalent events such as `GIVE` and `SHOW` both involve three arguments, but differ in intentional complexity.
- This project tests whether infants parse these events differently across development.

<figure class="project-figure project-figure-single project-figure-prior">
  <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-prior-work.png' | relative_url }}?v=20260423c" alt="Prior work framing on event structure and argument representation">
  <figcaption>Conceptual and developmental framing for verb-argument structure and trivalent event parsing.</figcaption>
</figure>

## Research Questions

- Do gaze transition patterns change from 7 to 11 months, specifically away from `Toy↔Body` and toward `Face↔Face` transitions?
- Do `GIVE` and `SHOW` differ in the developmental trajectory of these gaze patterns?

## Method

<figure class="project-figure project-figure-single project-figure-experiment">
  <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-experiment-stimuli.png' | relative_url }}?v=20260423c" alt="Experiment stimuli examples for GIVE and SHOW conditions">
  <figcaption>Experiment stimuli examples used across HUG, GIVE and SHOW conditions.</figcaption>
</figure>

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

## Results Summary

- In `GIVE`, `Face↔Face` transitions increased with age (`beta=0.053`, `p=.001`), while `Toy↔Body` transitions decreased (`beta=-0.078`, `p=.006`).
- In `SHOW`, `Face↔Face` transitions also increased (`beta=0.033`, `p=.007`), and `Toy↔Body` transitions decreased (`beta=-0.075`, `p<.0001`).
- Toy-to-face transitions showed a stronger age trend for `SHOW` than for `GIVE`.
- By 10-11 months, infants approached adult-like patterns for `GIVE` but remained less adult-like for `SHOW`.

## Result Figures

<div class="project-figure-grid">
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-give-condition.png' | relative_url }}?v=20260423c" alt="GIVE condition age-trend plots">
    <figcaption>GIVE condition: age-related increases in face-oriented transitions and decreases in toy-body transitions.</figcaption>
  </figure>
  <figure class="project-figure">
    <img src="{{ '/media/research/eye-tracking-study-on-infant-event-representation/figure-show-condition.png' | relative_url }}?v=20260423c" alt="SHOW condition age-trend plots">
    <figcaption>SHOW condition: similar directional changes, but with slower convergence to adult-like transition patterns.</figcaption>
  </figure>
</div>

## Take-Away

- Infants develop adult-like event parsing for `GIVE` by around 10-11 months, but not for `SHOW`.
- This suggests physical transfer is parsed before events requiring deeper understanding of intention.
- The pattern converges with Gordon (2003): infants dishabituated to toy removal in GIVE but not SHOW.
- A developmental shift from `Toy↔Body` to `Face↔Face` transitions may reflect emerging intentionality and theory of mind.
- These changes may scaffold later verb-argument structure acquisition.

## Poster

Poster presented at 2026 Cognitive Development Society Meeting.

- [View or download poster PDF]({{ '/docs/research/infant-event-representation-poster.pdf' | relative_url }})

<div class="resume-container">
  <iframe class="resume-embed" src="{{ '/docs/research/infant-event-representation-poster.pdf' | relative_url }}" title="Eye-Tracking Study on Infant Event Representation poster"></iframe>
</div>
