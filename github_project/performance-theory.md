---
layout: page
title: Performance theory
---

# Performance theory

> Interpretive framework for ECHOCHIMERA. This document describes how the
> instrument is intended to be performed and understood; it is not an
> empirical study of audiences.

## 1. Listening as composition

ECHOCHIMERA begins with listening, not with generation. The performer's
sound is analysed into pitch, energy, onset and timbre; those features
enter a decision process before any note is produced. Listening is
therefore the first compositional act.

The instrument does not treat input as a trigger. It treats input as
evidence: is the performer playing? is there a stable pitch? is the
gesture strong enough to answer? The answer may be no.

## 2. Constrained agency

The system has agency, but not unlimited agency. Its decisions are
bounded by:

- an energy/onset gate;
- a response probability;
- a character with a duration and density range;
- a response contract with maximum starts and tail;
- a MIDI contract that forbids program changes and SysEx;
- a note ledger that closes stuck notes.

This is the central performance idea: **the instrument can refuse**.
Refusal is not a failure of the system; it is part of its voice.

## 3. Seven characters

The performer does not select a patch. The system inhabits a character:

```text
HELD        slow, sparse, isolated register
HELD_PULSE  held tone with slow pulses
GESTURE     short, wide, statistical
CLUSTER     dense, narrow, beating
ECHO        answering with the performer's material
FRAGMENT    isolated fragments, no continuity
SILENCE     the response is the absence of response
```

Character is audible in duration, density, silence ratio, articulation
and register. The performer can bias the choice, but cannot fully
determine it.

## 4. Refusal and silence

`SILENCE` is a first-class response. It is not an empty buffer or a
muted error. The instrument may decide that the correct musical answer is
to leave the space open.

In performance, this changes the performer's task. The musician is not
filling a loop; they are negotiating with a system that can wait. Silence
becomes a shared material rather than an absence.

## 5. Latency, anticipation and surprise

Latency is not only a technical value. It is a dramaturgical quantity:

- too short: the system feels like a mirror or a trigger;
- too long: the system feels disconnected;
- variable: the system feels alive.

The interface exposes latency in milliseconds, but the performer should
judge it by feel. The ResponsePlanner adds a deliberate delay and tail so
that the answer has a place to arrive.

## 6. Error as material

Errors are part of the performance vocabulary:

- a note that does not speak;
- a MIDI port that disappears;
- a stuck note;
- a decision that arrives late;
- a silence that lasts too long.

The system provides `PANIC`, `NoteLedger` and explicit logs. Recovery is
part of the instrument's form. A performance that hides failure is less
honest than one that can recover in public.

## 7. The performer–system contract

The performer agrees to:

- listen to the answer before playing over it;
- leave room for refusal;
- treat silence as meaningful;
- not use the system as a backing track;
- stop when the system is in a failed state.

The system agrees to:

- not send program changes or SysEx;
- close notes it opens;
- expose its state;
- respect the configured channels;
- stop on panic.

This contract is documented in code, not only in prose.

## 8. Heautoscopy

The project's title uses *heautoscopy* as a metaphor for self-observation:
the performer sees their own listening reflected in the system's decision.
The interface makes that reflection visible through:

- the decision history;
- the last phrase;
- the pitch/response trace;
- the Markov graph;
- the harmony and rhythm panels.

The instrument is not a mirror that copies. It is a mirror that answers.

## 9. Stage dramaturgy

A performance can be organised as a sequence of agencies:

```text
1. the system listens
2. the system refuses
3. the system answers
4. the performer answers the answer
5. the system withdraws
6. the system fails and recovers
7. the system stops
```

This is not a fixed score. It is a set of possible states the performer
can expose or conceal.

## 10. What the audience hears and sees

The audience hears:

- the performer's material;
- the system's material;
- the space between them;
- the timbre of the synthesizer, which is outside the system's control.

The audience may see:

- the QuadPad surface;
- the decision history;
- the visualiser;
- the performer's hands and listening.

The interface should not explain the music. It should make the system's
agency legible without turning the performance into a demonstration.

## 11. Evaluation of a performance

A performance can be discussed through:

- **agency**: did the system make audible decisions?
- **refusal**: was silence used as material?
- **listening**: did the answer relate to the input?
- **risk**: did the system do something the performer did not expect?
- **recovery**: did failure remain performable?
- **balance**: did the system leave room for the human?

These are interpretive criteria, not benchmark scores.

## 12. Limits

The current implementation is monophonic in pitch detection, fixed to
4/4, and dependent on the synthesizer's timbre. It does not yet model a
room, a audience, or a second performer. The performance theory above is
therefore a frame for the existing instrument, not a claim that the
instrument already fulfils it in every context.
