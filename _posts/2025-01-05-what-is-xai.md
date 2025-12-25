---
layout: post
title:  "Why Black Box Models Are Dangerous: Intro to XAI"
date:   2025-01-05 09:00:00 +0100
categories: [AI, Research]
---

Deep learning models are often called "black boxes" because even their creators don't fully understand *why* they make specific decisions. In safety-critical fields like aerospace (where I work at DLR), this is unacceptable.

## What is XAI?

**Explainable AI (XAI)** is a set of processes and methods that allows human users to comprehend and trust the results and output created by machine learning algorithms.

### Key Techniques
1.  **LIME (Local Interpretable Model-agnostic Explanations)**: Approximates the black box locally with a simpler model.
2.  **SHAP (SHapley Additive exPlanations)**: Uses game theory to assign credit to features.

> "If you can't explain it, you shouldn't deploy it in a critical system."

In my next post, I will share code snippets on how to implement SHAP with PyTorch.
