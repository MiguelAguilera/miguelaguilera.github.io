---
layout: post
title: "Inferring Entropy Production in Many-Body Systems Using Nonequilibrium Maximum Entropy"
author: "Miguel Aguilera"
categories: blog
tags: [paper]
image: inferring-entropy-production.png
---


A familiar frustration in nonequilibrium physics is that **entropy production is the quantity you want**, but in high dimensions it is often the quantity you *cannot* estimate: the state space is huge, the dynamics are partially observed, memory effects creep in, and the usual estimators collapse under computational or statistical load.

We just had a paper accepted in *Physical Review Letters* that takes a different route:

> **Infer dissipation without reconstructing the full dynamics** — by combining a nonequilibrium analogue of Maximum Entropy with convex duality, using only samples of trajectory observables. Instead of estimating high-dimensional probability currents or rate matrices, the method:
- works directly with **trajectory-level observables** (e.g., spatiotemporal correlations),
- yields **trajectory-level entropy production** and **lower bounds on average entropy production**,
- extends naturally to **non-Markovian** settings with long memory,
- and supports a **hierarchical decomposition** of dissipation into contributions from different interaction structures.

There is also an intuitive physical reading: the construction connects to a **thermodynamic-uncertainty-relation-like** interpretation, where dissipation is constrained by measurable fluctuations/correlations.


Our method suggests a pragmatic workflow for real high-dimensional data:
1. pick the observables you actually trust (correlations, coarse-grained statistics),
2. fit the best nonequilibrium MaxEnt surrogate consistent with those constraints,
3. read out dissipation (and structured lower bounds) without pretending you learned the full world.

In the paper, we demonstrate its performance on 1) a disordered nonequilibrium spin model with **1000 spins**, and 2) a large **neural spike-train** dataset.


* **Aguilera** M, Ito S & Kolchinsky A (2026). [Inferring Entropy Production in Many-Body Systems Using Nonequilibrium Maximum Entropy](https://journals.aps.org/prl/pdf/10.1103/xgkj-dxzh). _Physical Review Letters_ **136**, 077101.  \
[![DOI](https://img.shields.io/badge/DOI-10.1103/xgkj--dxzh-lightgreen.svg)](DOI: https://doi.org/10.1103/xgkj-dxzh)


**Abstract**

We propose a method for inferring entropy production (EP) in high-dimensional stochastic systems, including many-body systems and non-Markovian systems with long memory. Standard techniques for estimating EP become intractable in such systems due to computational and statistical limitations. We infer trajectory-level EP and lower bounds on average EP by exploiting a nonequilibrium analogue of the maximum entropy principle, along with convex duality. Our approach uses only samples of trajectory observables, such as spatiotemporal correlations. It does not require reconstruction of high-dimensional probability distributions or rate matrices, nor impose any special assumptions such as discrete states or multipartite dynamics. In addition, it may be used to compute a hierarchical decomposition of EP, reflecting contributions from different interaction orders, and it has an intuitive physical interpretation as a “thermodynamic uncertainty relation.” We demonstrate its numerical performance on a disordered nonequilibrium spin model with 1000 spins and a large neural spike-train dataset.
