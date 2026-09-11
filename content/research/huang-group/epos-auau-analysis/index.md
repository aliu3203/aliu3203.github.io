---
title: 'epos-auau-analysis'
date: 2026-09-03
summary: 'Scripts for computing observables and the autonomous scheduler'
links:
  - type: github
    url: https://github.com/aliu3203/epos-auau-analysis
    label: Github Repo
---

EPOS is an event generator, which means I know the true reaction plane of every event it
produces. Real data does not come with that, so the methods used on it have to reconstruct
the plane and hope the reconstruction is good. Having the true answer available makes this a
useful place to check how much those methods actually recover.

I generate Au+Au collisions at 200 GeV and run the analysis in ROOT. So far that has meant
v2 of pions, kaons and protons measured against both the true reaction plane and a
reconstructed event plane, and the event shape selection method from arXiv:2307.14997, which
is one of the ways people try to subtract the flow background out of a CME measurement.

The current dataset is about 84,000 events, all in the 30-40% centrality range. The v2
results come out where you would want them to: mass ordering at low pT, baryons above mesons
higher up. The reconstructed event plane sits noticeably above the true one and the gap grows
with pT, which is non-flow leaking in rather than anything physical.

A fair amount of the work has been on the data itself. Several branches in the output tree
are named misleadingly, so a chunk of the early effort went into figuring out which one is
really the reaction plane before any of the numbers meant anything.
