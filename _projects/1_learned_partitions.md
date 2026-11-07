---
layout: page
title: Learned partitions for black-box optimization
description: Search faster by learning where the function actually varies (ICML 2025)
img: assets/img/publication_preview/adaptive_partitioning.png
importance: 1
category: research
related_publications: true
---

Many black-box functions with dozens of inputs really depend on only a few combinations of them. Optimistic optimization algorithms such as SequOOL split the search space into cells and refine the promising ones, but their splits are fixed in advance, so they pay for every dimension.

This project learns the low-dimensional subspace from a small number of evaluations, using a neural network surrogate, and then partitions along it. For functions that vary in an $m$-dimensional subspace of $d$ dimensions, the regret improves from $\tilde{O}(n^{-1/d})$ to $\tilde{O}(n^{-\beta/d})$ with $\beta = 1 + \frac{d-m}{2m-1}$. The method is competitive on standard benchmarks, and the paper introduces LLM weight quantization as a new black-box optimization task.

- **Paper:** [ICML 2025](https://proceedings.mlr.press/v267/sunkara25a.html) · [arXiv](https://arxiv.org/abs/2610.04039) · [project page](https://raja-sunkara.github.io/Learned-Partitions-SequOOL/)
- **Code:** [GitHub](https://github.com/raja-sunkara/Learned-Partitions-SequOOL). A pip-installable package with a SciPy-style `minimize`, an ask-tell interface and an Optuna sampler.

{% cite sunkara2025adaptive %}
