---
layout: page
title: YOGA
description: A lightweight object detector for edge devices (Pattern Recognition 2023)
img: assets/img/publication_preview/yoga.png
importance: 3
category: research
related_publications: true
---

YOGA is a YOLO-style detector built for low-end hardware such as the NVIDIA Jetson Nano. Its **CSPGhostNet** backbone learns half of each layer's feature maps with ordinary convolutions and generates the other half with cheap linear operations. Its **AFF-PANet** neck fuses multi-scale features with attentional feature fusion.

Compared with more than ten detectors on COCO, YOGA gives the best trade-off between size and accuracy: up to 22% higher AP with 23–34% fewer parameters and FLOPs. The four model sizes range from 1.9M parameters (32.3 AP) to 33.6M parameters (48.9 AP).

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/publication_preview/yoga.png" title="YOGA architecture" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

- **Paper:** [Pattern Recognition](https://doi.org/10.1016/j.patcog.2023.109451) · [arXiv](https://arxiv.org/abs/2307.05945)
- **Code:** [GitHub](https://github.com/TrustAIoT/YOGA_object-detection). Pretrained COCO weights load in one line with `torch.hub.load("TrustAIoT/YOGA_object-detection", "yoga_s")`, and there is a [Colab quick start](https://colab.research.google.com/github/TrustAIoT/YOGA_object-detection/blob/main/YOGA_quickstart.ipynb).

{% cite sunkara2023yoga %}
