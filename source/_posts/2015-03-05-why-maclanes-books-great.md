---
layout: post
title: "Why MacLane's book's great"
date: 2015-03-05 09:34:33 +0100
comments: true
published: false
categories: ["Things I don't yet understand", "Category theory"]
---

Mathematicians claim MacLane's book on category theory is excellent. Now that I
start understanding why, I'd like to share what I understood with you. Since
years, I have been studying category theory on and off, for its applications to
programming language theory. After reading parts of Pierce, Barr and Wells and
Awodey, I recently approached MacLane's famous textbook, and I finally started
getting why every mathematician recommends MacLane, and why (currently) no book
for non-mathematicians is like it. So I'll try to convey what I appreciated.
While I don't advocate it as an introduction to category theory (see instead the
excellent advise from [Peter Smith](http://www.logicmatters.net/categories/)).

Caveat: I am not actually a mathematician, so what follows might be inaccurate.

## Mathematics provides for more compelling, and even concrete examples

When applying category theory to functional programming, how many really
different categories do we have? In the end, it often all boils down to the
semantics of programs, or with programs up to some equivalence. You can have
categories for different languages; you can try considering the List functor in
the category of datatypes for a non-polymorphic language, that maps the datatype
of integers to the datatype of lists of integers by source code generation. If
you're lucky, maybe you deal with syntax in the category of substitutions.

Instead, take (the category of) solids which can have holes. You can study paths
from a base point through these holes, identify them if they can be deformed
into each other, and allow composing them or inverting them---this way, you get
the [*fundamental group*](https://en.wikipedia.org/wiki/Fundamental_group). This
construction has multiple applications. MacLane will point out that this
construction is a functor, mapping a solid with potential holes to its
fundamental group. And category theory (as usual) will force you to also
consider how to map arrows in those categories.

## MacLane does not hide definitions away

Adjoint functors are motivated and exemplified already in the introduction.
Reading it is challenging, but it offers an enlightening summary of category
theory.

I can also recommend his discussions of duality and of size issues for
categories (in his first chapters). I believe they are clear and complete while
being accessible—in fact, they were clearer to me, because the discussion of
duality is less vague, while his handling of size has less arbitrary
restrictions.

## He gives crystalline and concise definitions

His definitions are concise and thus have less detail to remember.

## He's the founder

He has thus both the historical perspective and the motivational insight into
concepts.
