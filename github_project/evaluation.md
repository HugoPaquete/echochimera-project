---
layout: page
title: Evaluation
---

# Evaluation

This page reports what has been measured and what has not. It is a public
summary, not a lab notebook.

## Software

| Check | Result |
|---|---:|
| test suite | **359 passed** |
| selftest | **10/10** |
| Qt smoke | exit 0 |
| executable selftest | exit 0 |

## Pitch

- maximum sine calibration error: **1.92 cents**;
- missed pitches: 0/6;
- noise false positives: 0/30.

The detector is monophonic.

## Rhythm

Internal audit:

- 85 scenarios;
- 332 planned rhythm events;
- 332 observed on channel 9/10;
- first onset 0.375 s;
- mean velocity 58;
- range 51–79.

## Presets

- 17 presets;
- 136 structural pairs;
- closest pair: `partial_glitch` / `data_stream`, distance 0.173;
- scale changes affect 12/17;
- five structural exceptions: four tonic-only, one intentional silence.

The preset metric is structural, not perceptual.

## Lifecycle

Eight start/stop cycles, no errors, one thread at rest.

## Interface

Twenty-one screenshots covering seven windows, nine Lab tabs, three
isolated surfaces, a decision table and a contact sheet.

## Not measured

- target-DAW latency;
- Kontakt behaviour;
- 30–60 minute hardware soak;
- audience response;
- performer interviews;
- polyphonic pitch.

## Interpretation

The evidence supports stability and MIDI/rhythm connectivity. It does not
establish that the presets sound distinct to listeners or that latency is
acceptable in a specific setup.
