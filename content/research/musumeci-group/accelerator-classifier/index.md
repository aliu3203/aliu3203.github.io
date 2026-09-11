---
title: 'Accelerator Classifier'
date: 2026-09-03
summary: 'Source code for the scraper + classifier'
links:
  - type: github
    url: https://github.com/aliu3203/acceleratorClassifier
    label: Github Repo
---

The question was how much work on new acceleration techniques is showing up outside the
accelerator journals, and whether that share is growing. Answering it by hand means reading a
lot of abstracts, so I trained something to do the first pass instead.

The scrapers pull from Physical Review Accelerators and Beams along with a short list of high
impact journals by ISSN, Nature and Science and PRL among them. Training labels come from
keyword matching on titles and abstracts, plus the assumption that anything published in PRAB
counts as accelerator work. A multinomial naive Bayes model then sorts a paper into one of
three buckets: not accelerator, accelerator, or new acceleration technique. The analysis
scripts run the saved model over fresh unlabeled scrapes and plot the counts.

The labels it learns from are noisy, since they started from keywords and not from anyone
reading the paper. So the output is worth looking at as a trend and not worth trusting on any
single paper.
