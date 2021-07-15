---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

<!--{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
-->

## Table of Contents

1. [PyTorch Connectomics](#pytorch_connectomics)
2. [Connectomics Challenges](#challenges)
3. [Two-Stream Active Query Suggestion](#two_stream_active)

------------------------------------------------------------------------------

## PyTorch Connectomics <a name="pytorch_connectomics"></a>

### Introduction

The field of ***connectomics*** aims to reconstruct the wiring diagram of the brain by mapping the neural connections at the level of individual synapses. Recent advances in electronic microscopy (EM) have enabled the collection of a large number of image stacks at nanometer resolution, but the annotation requires expertise and is super time-consuming. Here we provide a deep learning framework powered by [PyTorch](https://pytorch.org/) for automatic and semi-automatic image segmentation in connectomics. This repository is actively under development by Visual Computing Group ([VCG](https://vcg.seas.harvard.edu)) at Harvard University.

### [[Documentation](https://connectomics.readthedocs.io/)] [[GitHub](https://github.com/zudi-lin/pytorch_connectomics#pytorch-connectomics)]

<a href="https://connectomics.readthedocs.io/en/latest/">
<img style="float:left;margin:10px 10px 0px 0px" src="/files/figures/misc/pytc_logo_square.png" alt="PyTC Logo" width="160" height="160">
</a>

We are committed to providing a "user-centric" open-source package to help neuroscience researchers working on different biological structures and imaging modalities. Currently, besides installation guidance and package references, we provide several tutorials covering both semantic and instance segmentation for [neurons](https://connectomics.readthedocs.io/en/latest/tutorials/neuron.html), and other biological structures like [synapses](https://connectomics.readthedocs.io/en/latest/tutorials/synapse.html) and [mitochondria](https://connectomics.readthedocs.io/en/latest/tutorials/mito.html). We are also working on imaging artifacts detection, nuclei segmentation, and blood vessel segmentation. Please join our Slack community using this [link](https://join.slack.com/t/pytorchconnectomics/shared_invite/zt-obufj5d1-v5_NndNS5yog8vhxy4L12w).
<br/>

------------------------------------------------------------------------------

## Connectomics Challenges <a name="challenges"></a>

### MitoEM Challenge: Large-scale 3D Mitochondria Instance Segmentation

<a href="https://mitoem.grand-challenge.org">
<img style="float:left;margin:10px 10px 0px 0px" src="/files/figures/challenges/mitoem_logo.png" alt="MitoEM Logo" width="160" height="160">
</a>

The task is the ***3D mitochondria instance segmentation*** on two 30x30x30 μm^3 datasets, 1000x4096x4096 in voxels at (30, 8, 8) nanometer (nm) resolution. The electron microscopy (EM) image volumes are acquired from a rat (MitoEM-R) and a human (MitoEM-H) tissue, respectively. The mitochondria can display a complex morphology, *e.g.*, mitochondria-on-a-string (MOAS) instances that are connected by thin microtubules, and multiple instances can entangle with each other. Our [MitoEM challenge](https://mitoem.grand-challenge.org) is held at [IEEE ISBI 2021](https://biomedicalimaging.org/2021/).

### NucMM Challenge: 3D Neuronal Nuclei Instance Segmentation at Sub-Cubic Millimeter Scale

<a href="https://nucmm.grand-challenge.org/">
<img style="float:left;margin:10px 10px 0px 0px" src="/files/figures/challenges/nucmm_logo.png" alt="NucMM Logo" width="160" height="160">
</a>

The task is the ***3D neuronal nuclei instance segmentation*** on two sub-cubic millimeter scale datasets, one 0.1 mm^3 electron microscopy (EM) volume containing nearly the entire zebrafish brain with around 170,000 nuclei; and one 0.25 mm^3 micro-CT (uCT) volume containing part of a mouse visual cortex with about 7,000 nuclei. With two imaging modalities and significantly increased volume size and instance numbers, we discover a great diversity of neuronal nuclei in appearance and density, introducing new challenges to the field. Please check our [paper](https://arxiv.org/abs/2107.05840) for details.

### AxonEM Challenge: 3D Axon Instance Segmentation of Brain Cortical Regions

<a href="https://axonem.grand-challenge.org/">
<img style="float:left;margin:10px 10px 0px 0px" src="/files/figures/challenges/axonem_logo.png" alt="NucMM Logo" width="160" height="160">
</a>

The task is the ***3D axon instance segmentation*** on two 30x30x30 um^3 electron microscopy (EM) image volumes from the human and mouse cortex. Due to the complex morphology, an accurate reconstruction of cortical axons has become a major challenge in EM connectomics. We thoroughly proofread over 18,000 axon instances to provide dense 3D axon instance segmentation, enabling large-scale evaluation of axon reconstruction methods. In addition, we densely annotate nine ground truth subvolumes for training, per each data volume. Please check our [paper](https://arxiv.org/abs/2107.05451) for details.

------------------------------------------------------------------------------

## Two-Stream Active Query Suggestion for Active Learning in Connectomics <a name="two_stream_active"></a>

![Two-stream active](/files/figures/two_stream/two_stream_overview.png)

### Abstract

For large-scale vision tasks in biomedical images, the labeled data is often limited to train effective deep models.
Active learning is a common solution, where a query suggestion method selects representative unlabeled samples for annotation, and the new labels are used to improve the base model.
However, most query suggestion models optimize their learnable parameters only on the limited labeled data and consequently become less effective for the more challenging unlabeled data.
To tackle this, we propose a ***two-stream active*** query suggestion approach. In addition to the supervised feature extractor, we introduce an unsupervised one optimized on all raw images to capture diverse image features, which can later be improved by fine-tuning on new labels.
As a use case, we build an end-to-end active learning framework with our query suggestion method for 3D synapse detection and mitochondria segmentation in connectomics. With the framework, we curate, to our best knowledge, the largest connectomics dataset with dense synapses and mitochondria annotation.

### Publication

Zudi Lin, [Donglai Wei](https://donglaiw.github.io), [Won-Dong Jang](https://wdjang.github.io), Siyan Zhou, Xupeng Chen, [Xueying Wang](https://sites.google.com/view/snowxwang/home?authuser=0), Richard Schalek, Daniel Berger, [Brian Matejek](https://www.brianmatejek.com), Lee Kamentsky, Adi Suissa-Peleg, [Daniel Haehn](https://danielhaehn.com), [Thouis Jones](https://personal.broadinstitute.org/thouis/), Toufiq Parag, [Jeff Lichtman](https://lichtmanlab.fas.harvard.edu/people/jeff-lichtman) and [Hanspeter Pfister](https://en.wikipedia.org/wiki/Hanspeter_Pfister). "Two-Stream Active Query Suggestion for Active Learning in Connectomics." *European Conference on Computer Vision* (**ECCV**), 2020 [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123630103.pdf)][[Supp.](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123630103-supp.pdf)]

### Code

* Mitocondria Segmentation on the Lucchi Dataset [[Link](https://connectomics.readthedocs.io/en/latest/tutorials/mito.html#semantic-segmentation)]
* Synaptic Cleft Detection on the CREMI Dataset [[Link](https://connectomics.readthedocs.io/en/latest/tutorials/synapse.html#synaptic-cleft-detections)]
* Synaptic Polarity Detection on the EM-R50 Dataset [[Link](https://connectomics.readthedocs.io/en/latest/tutorials/synapse.html#synaptic-polarity-detection)]
* ***Two-Stream Query Suggestion*** Algorithm [[Link](https://github.com/zudi-lin/pytorch_connectomics/blob/master/scripts/tools/two_stream.py)]

### Acknowledgements

This project has been partially supported by NSF award IIS-1835231 and NIH award 5U54CA225088-03.

------------------------------------------------------------------------------
