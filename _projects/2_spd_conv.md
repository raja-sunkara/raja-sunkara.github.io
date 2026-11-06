---
layout: page
title: SPD-Conv
description: A CNN building block for small objects and low-resolution images (ECML PKDD 2022)
img: assets/img/publication_preview/spd_conv.png
importance: 2
category: research
related_publications: true
---

Strided convolutions and pooling throw away fine detail every time a CNN downsamples. That hardly matters on large, clean images, but it hurts on small objects and low-resolution inputs.

SPD-Conv replaces each of these layers with a **space-to-depth** step, which moves every 2×2 block of pixels into the channel dimension so nothing is discarded, followed by a **non-strided convolution**. It drops into most CNNs. In the paper, YOLOv5-SPD and ResNet-SPD outperform their baselines on small objects and low-resolution images, and the block is now widely used in YOLO-based detectors.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/publication_preview/spd_conv.png" title="SPD-Conv" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

- **Paper:** [ECML PKDD 2022](https://doi.org/10.1007/978-3-031-26409-2_27) · [arXiv](https://arxiv.org/abs/2208.03641)
- **Code:** [GitHub](https://github.com/LabSAINT/SPD-Conv), with YOLOv5-SPD, ResNet18-SPD and ResNet50-SPD.

{% cite sunkara2022no %}
