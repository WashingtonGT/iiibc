---
title: Foundation Model Foundry Ramp Plan
date: 2024-05-18
description: GPU allocation model that balances research batch jobs with interactive inference SLAs.
tags:
  - infrastructure
  - scaling
categories:
  - AI technology
---

Large clusters are now shared across six research squads plus two product inference groups. We outline a four-phase migration to pooled scheduling that keeps the launch cadence intact while also unlocking 20% higher GPU utilization.

## Control planes

A shared scheduler running atop Ray Serve gives researchers self-service access to 512-GPU shards with spot/flex mixes defined via policy. Product teams continue to pin critical inference services to on-demand nodes, but we carve out an emergency burst pool to satisfy surprise demo requirements.

## Funding model

Each division pre-pays for **baseline** capacity while the central AI office meters incremental boosts weekly. Finance receives a transparent ledger of GPU hours with tags by objective and owner, so they can forecast demand a quarter out.
