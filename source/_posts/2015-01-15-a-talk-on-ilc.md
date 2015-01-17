---
layout: post
title: "A talk on Incremental λ-Calculus"
date: 2015-01-15 08:18:48 +0100
comments: true
categories: [Research]
---

For my work on Incremental λ-Calculus (ILC), next week I'm visiting the
Paris-Diderot (Paris 7) University, and I'll have a chance of giving a talk at
their [PPS seminar](http://www.pps.univ-paris-diderot.fr/seminaire/). I'm very
excited about this visit, and I plan to talk about our progress since our PLDI
2014 paper.

Below the abstract of the talk. I plan to upload slides later.

### Incrementalizing λ-calculi by static differentiation: A theory of changes for higher-order languages and ongoing work

\[Joint work with Yufei Cai, Tillmann Rendel and Klaus Ostermann\]

**Abstract:**

If the result of an expensive computation is invalidated by a small change to the input, the old result should be updated incrementally instead of reexecuting the whole computation.
I'll give an overview of our approach to this problem, as presented in our recent paper [1], and discuss ongoing work.

We incrementalize programs using derivatives: A derivative maps changes in the program’s input directly to changes in the program’s output, without reexecuting the original program. We present a program transformation taking programs to their derivatives, which is fully static and automatic, supports first-class functions, and produces derivatives amenable to standard optimization.

We proved the program transformation correct in Agda for a family of simply-typed λ-calculi, parameterized by base types and primitives. A precise interface specifies what is required to incrementalize the chosen primitives.

In ongoing work, we are investigating different extensions:

- simplifying our correctness proofs using category theory and realizability;
- proving more optimizations correct using abstract types and parametricity;
- static memoization to improve performance, using a variant of call-by-push-value as an intermediate program representation.

I will briefly mention our progress on these extensions, together with open questions.

[1] PLDI 2014, <http://dl.acm.org/citation.cfm?id=2594304>.
