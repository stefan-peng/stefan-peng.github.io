---
title: Pipelined MIPS processor
date: Fall 2018
---

The final project for my CPR E 381 class was to develop a pipelined MIPS processor with hazard detection, forwarding, and ID-stage branch resolution. I designed this in VHDL with two other students. Using the single-cycle processor we had previously developed, we were able to add pipelines registers, additional components for the ID-stage branch resolution, a forwarding unit, and a hazard detection unit. The end result was a MIPS processor that had a higher throughput than our original single-cycle implementation.