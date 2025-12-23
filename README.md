#  Multi-Layer Explainability Framework for Foundation Model Anomaly Detection in Oral Histopathology
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org/)

## Overview

This repository contains the implementation of a novel 4-layer explainability framework that bridges the semantic gap between foundation model representations and clinically interpretable pathology concepts. Our system enables pathologists to understand *why* AI flags tissue as anomalous, addressing the critical trust barrier preventing clinical adoption of medical AI.

## Problem Statement

Foundation models like UNI2 achieve high accuracy in detecting oral cancers but remain "black boxes"—they cannot explain their decisions in clinical terms. This prevents pathologists from trusting and using these systems for cancer diagnosis, where understanding the reasoning is legally and medically essential.

## Our Solution

We developed a comprehensive explainability framework with four independent layers that systematically decode UNI2's 1536-dimensional embeddings:

1. **Layer 1: Visual Attention Analysis** - WHERE did the model focus?
2. **Layer 2: Feature Importance** - WHICH dimensions drive decisions?
3. **Layer 3: Clinical Interpretation** - WHAT do dimensions mean clinically?
4. **Layer 4: Prototype Comparison** - HOW different from normal tissue?

5. ### Key Innovation

Through rigorous correlation analysis, we discovered that abstract AI dimensions correspond to clinical concepts pathologists use daily:
- **Dimension 127** = Pink staining intensity (r=0.71, p<0.001)
- **Dimension 334** = Nuclear density (r=0.68, p<0.001)  
- **Dimension 891** = Architectural regularity (r=-0.65, p<0.001)



**ORCHID (Oral Cancer Histopathology Image Dataset)**
- **4,000+** H&E stained oral tissue images
- **Training:** 1,200 normal samples (semi-supervised)
- **Validation:** 2,800 mixed samples

