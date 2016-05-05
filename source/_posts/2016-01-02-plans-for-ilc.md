---
layout: post
title: "Plans for ILC"
date: 2016-01-02 03:37:04 +0100
comments: true
categories: Research
published: false
---

# Background

An incrementalized program computes output changes from input changes. With some
colleagues we've shown how to produce incrementalized programs out of
simply-typed λ-calculus programs. However, quite a few challenges remained. I
have not been idle on them; while I am not done yet, I feel I should talk about
the current progress.

# Summary of our PLDI'14 paper

In our paper we introduced the concept of change algebras: for each value, a
change algebra fixed a set of valid changes, leading to other values.

Moreover, we showed how to define change algebras for a few types, including
function types. Based on this theory, we designed a code transformation system
that could handle a nontrivial case study.

# After PLDI'14

Our paper left a number of questions open:

- No way to reuse intermediate results. Many incremental programs need reuse
  intermediate results computed while running the base program. As we described
  and as some readers observed, we provided no support for remembering such
  results. A relatively easy solution would be to memoize such intermediate
  results in a hash table, to find them later. However, such lookups have a cost
  which can be avoided, and maintenance of such hash tables raises nontrivial
  issues.

- No way to pattern match on function changes at runtime. Since function changes
  are functions, one can only apply them; there's no way to inspect them, even
  to check at runtime *if* they're nil changes or not.

  This was already an issue in our case study, though we still incrementalized
  it successfully by treading carefully around the issue. Mainly, we managed to
  apply static analysis to check if a function change was guaranteed to be nil.
  If anything, using functions allowed us to work on a small language,
  simplifying this analysis. However, if the analysis failed in proving
  statically a function change was nil, we were stuck.

  It took us a while to find a general approach against this: we should
  defunctionalize function changes. In fact, we might as well just
  defunctionalize the original program altogether.

- No support for algebraic data types.

- We didn't provide yet a way to talk about the equivalence of two changes.
- We did not really support polymorphism.

# Technical goals of the ILC project

One of my goals is to explore how well can one incrementalize programs
statically. That is, instead of providing incremental semantics using a
non-standard interpreter, generate instrumented code in a standard semantics
that provides incremental behavior. One goal is to

# Goals of the ILC project

As typical during research, I have been understanding better for what is my research useful.


Incrementalized programs can be useful if they are faster; however, there can be
further reasons. Without incrementalization, we could produce output changes by
running a diff-like tool on the output; however, not only can that be expensive,
but it might not show how the input changes propagate to output changes.

Moreover,

# My vision for this project

See how much
