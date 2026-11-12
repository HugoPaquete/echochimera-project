---
layout: page
title: Technical paper
---

# ECHOCHIMERA: a constrained-agency instrument for human–AI performance

**Hugo Paquete**  
INET-md / University of Aveiro and Absonus Lab  
AI as Catalyst / MECS

> Technical preprint. Not peer-reviewed.

## Abstract

ECHOCHIMERA is a real-time MIDI instrument for human–AI performance. It
listens to a performer, decides whether to answer, selects one of seven
musical characters, plans a bounded response, and performs it through an
allow-listed MIDI router. The contribution is a constraint architecture:
decision gates, response contracts, character-specific duration/density
and a note ledger make agency audible and recoverable.

The system combines a phenomenological corpus, a Markov model,
scale-aware harmony, a 16-step rhythm layer, live controllers and an
explicit performance interface.

## 1. Introduction

Generative systems often maximise output. ECHOCHIMERA starts from the
opposite question: when should an AI performer not answer?

The instrument is a turn-taking system. It listens, decides, responds or
refuses, and returns to listening. Its identity is produced by
constraints rather than by an unlimited generator.

## 2. System

```text
audio → features → decision → response contract
      → character → corpus/Markov → harmony/rhythm
      → scheduler → MIDI router → note ledger
```

The UI reads immutable snapshots, not the audio thread. Windows:
QuadPad, Decision, Phrase, Session, Rhythm, Visualiser, Console; Lab:
Routing, Parameters, Harmony, Live, CC, Scenes, Memory, Help, About.

## 3. Musical model

Seven characters define duration, density, silence and articulation. The
system contains 38 scale definitions. Tonal characters are snapped to the
active scale; gesture/noise/cluster material keeps its corpus intervals
until the scale pass.

Rhythm is 4/4, one bar, 16 steps. Corpus material preserves its own
timing; the grid controls Markov material. Seventeen presets force
operator, aesthetic and corpus mix.

## 4. Performance theory

The performer negotiates with a system that can refuse. Silence is a
valid answer. Latency, error, panic and recovery are part of the
instrument's form.

## 5. Evaluation

- 359 tests passing;
- selftest 10/10;
- pitch error ≤ 1.92 cents on sine calibration;
- 8 start/stop cycles with no thread leak;
- 17 presets and 136 structural pairs;
- 12/17 presets change with scale;
- 21 GUI screenshots.

These are engineering and structural measurements, not audience data.

## 6. Limitations

- monophonic pitch detection;
- fixed 4/4;
- no controlled listening study;
- five tonic-only/silent preset cases;
- no measured target-DAW latency;
- self-signed Windows executable.

## 7. Contribution

1. A constraint-first architecture for human–AI performance.
2. A theory-grounded character mapping.
3. A transparent MIDI/CC contract with note safety.
4. A reproducible documentation and screenshot pipeline.
