---
layout: post
title: "Term Representations for Metaprogramming: Comparing CBPV versus Monadic Calculi and A-normal form"
date: 2014-12-23 21:06:51 +0100
comments: true
published: false
categories: ["programming languages", research]
---

CBPV (call-by-push-value), while designed for theoretical reasons, is a useful
improvement over monads for representing programs inside metaprograms.

It was designed as a calculus for effectful programs, not for pure ones, but
that's misleading: it applies to pure programs as well, at the very least
because most so-called "pure" programming languages (say, Haskell) allow
nonterminating programs; and nowadays, many scholars concur that it's useful to
treat nontermination just as a side effect.

Moreover:

1. many metaprograms need to represent the evaluation order explicitly in their
program representation (for instance, compilers need do that because programs
running on CPUs have a specific evaluation order)
2. to represent evaluation order explicitly, it's best to start from calculi for
effectful programs, even for programs that are anyway pure.

CBPV is an alternative to A-normal form and to the Moggi monadic calculi (like
the computational lambda calculus).

# A summary of CBPV

# Discussion
<!-- Move the above at the end, and remove this paragraph. -->
Concretely, one core difference is between an application `M N` in lambda
calculus and monadic bind `let x = N in M x`; the first syntax does not specify
whether `M` or `N` is evaluated first, while the second has a specific
evaluation order.

#

semanticists are mostly interested in the results of programs, so for pure typed lambda-calculi evaluation order makes no difference; calculi that
Accordingly, making evaluation order explicit would complicate their calculi without helping studying 

, simply because evaluation order can make a
difference for performance.

The $\lambda$-calculus is cool because it unifies programs and data. However, compilers trying to understand

In fact, since compilers typically make evaluation order explicit and deal with 

Nowadays theorists understand purely functional programs by understanding $\lambda$-calculi, and intermediate representations in metaprograms (such as compilers) for functional programming languages are inspired by $\lambda$-calculi.



I've been recently studying different core languages for effectful programs for
use as program representations and for program transformations.

Thanks to their use in Haskell, many functional programmers are used to representing effectful programs using monads; Haskell programmers even use monads directly! However, researchers 

I think 


In particular,
I'm becoming familiar with the differences between call-by-push value (by Levy)
and monadic calculi (introduced by Moggi and also studied by Filinski).

The literature is rather theoretical, and mostly aimed at semanticists. I've been studying this literature to use these calculi as an intermediate representation in a compiler.

Some existing literature establishes that 

My current understanding is the following:
- what is the relation with ANF?
- what is the difference between CBPV 

I claim that:
- 


# Digression: Why are these the best representation?

Generally, if you care about having a simple representation that is powerful,
you care about elegance; since the science of creating elegant (and precise)
concepts is mathematics, you often want to look at what mathematicians have come
up with. (This point deserves a far larger essay, but I'll keep it short for
now).

Furthermore, I claim that to represent programs with their evaluation order, you
should look at the mathematics of languages with effects. This might sounds
surprising, and the reason might be called sociological.

The mathematicians working in the area are the semanticists, who work on program
meaning, not so much on the needs of compiler writers. Since evaluation order
does not affect the meaning of pure programs, an elegant semantics of pure
programs must ignore evaluation order, and a term language to represent such
meaning should not highlight the evaluation order. On the contrary, since
evaluation order does affect the meaning of effectful programs, both a semantics
and a term language for effectful programs should deal explicitly with
evaluation order.

<!--
Outline:
- relation with ANF
- why functions are computations, and the eta-law for functions.

-->
