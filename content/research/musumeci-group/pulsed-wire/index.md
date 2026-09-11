---
title: 'Pulsed Wire'
date: 2026-09-03
summary: 'Measuring the field of permanent magnet quadrupoles with a pulsed wire, and the alignment work that has to happen first.'
links:
  - type: github
    url: https://github.com/aliu3203/pulsedWire
    label: Code
---

To map the field of a permanent magnet quadrupole, we string a thin copper wire through it
and send a current pulse down the wire. The field kicks it, a displacement travels along the
wire, and a photodiode watches the wire move across a laser. The signal that comes back tells
you about the field the wire passed through.

Most of the difficulty is not in the measurement. It is in the setup. The wire has to sit on
the magnetic axis to within microns, and if it does not, a good part of what you measure is
your own misalignment rather than the magnet. So most of my time goes into alignment
procedures and into checking that things like tension, sag and pulse shape repeat from run to
run.

The code in the repo is the data collection half. It talks to the oscilloscope over serial and
pulls waveforms back as binary blocks instead of parsing the ASCII output, which is both
faster and less fragile, then saves the traces for later.
