---
title: Training neural networks on the edge
theme: solarized
revealOptions:
    transition: 'fade'
---
# Training neural networks on the edge

Navjot Kukreja, Alena Shilova

Imperial College London, INRIA Bordeaux

---

Also:

 - Olivier Beaumont
 - Jan Huckelheim
 - Nicola Ferrier
 - Paul Hovland
 - Gerard Gorman

---

## Background

---

<img src="figures/seismic_waves.png" alt="drawing" width="1600"/>
Seismic Imaging
---

![](figures/dataflow.png)

Typical data flow pattern for adjoint problems

---

![](figures/checkpointing-all.png)

Memory consumption during an adjoint problem

---

Checkpointing (Revolve)

<iframe src="http://127.0.0.1:5000" width="100%"> </iframe>

---

Where else do we see the same data-access pattern?
![](figures/VGG_neural_network.png)

<sub><sup>VGGNet</sub></sup>

---

## Array of Things

![](figures/AoT.jpg)

---
## Waggle Payload Computer
- ODROID XU4 based on the Samsung Exynos5422 CPU
- four A15 cores, four A7 cores
- Mali-T628 MP6 GPU that supports OpenCL, 2GB
LPDDR3 RAM
- attached flash storage

---


## Viewpoint problem

---

## Student-teacher model

---

## Memory required to train ResNet 

---

![](figures/image_224.png)

Memory required (GB) for image size $224 \times 224$

---

![](figures/batch_1.png)

Memory required (GB) for batch size 1

---

![](figures/batch_8.png)

Memory required (GB) for batch size 8

---

## Checkpointing

---

Introduce Checkpoint Sequential

---

Comparison of Checkpoint sequential and Revolve

![](figures/batch_imagesize224_1.png)

Batch Size: $1$, Image Size: $224 \times 224$

---

![](figures/batch_imagesize224_8.png)

Batch Size: $8$, Image Size: $224 \times 224$

---

![](figures/batch_imagesize500_1.png)

Batch Size: $1$, Image Size: $500 \times 500$

---

![](figures/batch_imagesize500_8.png)

Batch Size: $8$, Image Size: $500 \times 500$

---
Practical implementation
