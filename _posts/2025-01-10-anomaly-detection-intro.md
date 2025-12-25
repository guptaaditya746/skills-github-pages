---
layout: post
title:  "Detecting the Invisible: Time Series Anomaly Detection"
date:   2025-01-10 10:30:00 +0100
categories: [Machine Learning, Tutorial]
---

How do you find a needle in a haystack when the haystack is moving at 100mph? That's what time-series anomaly detection feels like.

## The Challenge
Industrial sensors generate terabytes of data. Anomalies—signs of failure—are rare, making this an "unbalanced dataset" problem.

### Common Approaches
* **Statistical**: Z-score, Moving Averages (Simple but limited).
* **Autoencoders**: Neural networks that learn to compress and reconstruct data. High reconstruction error = Anomaly.

I am currently experimenting with **Transformers** for this task. The attention mechanism helps the model focus on relevant past time steps.
