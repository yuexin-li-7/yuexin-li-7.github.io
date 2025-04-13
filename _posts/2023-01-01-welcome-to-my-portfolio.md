---
layout: post
title: "Columbia AI Summit - Eye-Track-ML Poster Presentation"
date: 2023-01-15 14:00:00 -0500
categories: [academic, research]
---

I'm excited to share my recent experience presenting at the Columbia AI Summit, where I showcased our Eye-Track-ML project with a research poster.

<div style="text-align: center; margin-bottom: 2rem;">
  <img src="{{ '/media/signal-2025-04-13-163814.jpeg' | relative_url }}"
       alt="Eye-Track-ML Poster Presentation"
       style="max-width: 100%; height: auto;" />
  <p>
    <a href="{{ '/docs/Columbia AI Summit 2025 - Eye-Track-ML.pdf (1).pdf' | relative_url }}" target="_blank">
      Download Poster PDF
    </a>
  </p>
</div>

## Eye-Track-ML: A Machine Learning Pipeline for Automated Frame-by-Frame Coding of Eye-Tracking Videos

Our project, Eye-Track-ML, is a pipeline for automating eye-tracking video analysis using computer vision models, YOLO and SAM. We developed this solution to address the challenge of manually coding over 6+ hours of video data (600,000 frames) from our infant event representation study. The pipeline combines YOLOv11 for image classification and object detection with SAM2.1 for object segmentation.

### Key Achievements

- For event labeling, our pipeline achieves 100% accuracy
- For object labeling, we achieve ~94.26% accuracy
- This means approximately 94% of the object coding can be automated, drastically reducing manual labor

### The Pipeline Process

Our pipeline involves six sequential steps:

1. Breaking videos into frames
2. Classifying events
3. Detecting objects
4. Mapping gaze positions to semantic entities
5. Consolidating results into participant datasheets
6. Verifying results

The combined SAM+YOLO approach with 10px mask dilation achieves 94.24% accuracy, outperforming the YOLO-only approach by 5.36%.

### Human-in-the-Loop Verification

Despite the high accuracy of our automated approach, we found that human verification remains necessary for detecting subtle patterns and edge cases. However, our system establishes a strong baseline for consistency, requiring human verifiers to correct only about 6% of data points. This is a dramatic reduction in manual labor, potentially transforming how eye-tracking studies are conducted in cognitive neuroscience research.

### Summit Experience

The Columbia AI Summit provided an excellent opportunity to connect with other researchers and receive valuable feedback on our work. The interdisciplinary nature of the conference allowed us to discuss potential applications beyond our initial use case and explore collaborative opportunities with teams working on similar challenges in different domains.

### Resources

For those interested in learning more about the technologies used in our pipeline:

- [YOLO documentation](https://docs.ultralytics.com/)
- [Segment Anything Model (SAM) repository](https://github.com/facebookresearch/segment-anything)
- [How to train YOLOv11 on custom data](https://blog.roboflow.com/yolov11-how-to-train-custom-data/)
- [Fine-tuning SAM 2.1](https://blog.roboflow.com/fine-tune-sam-2-1/) 