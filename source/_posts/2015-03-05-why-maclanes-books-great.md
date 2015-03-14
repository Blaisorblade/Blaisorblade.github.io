---
layout: post
title: "Why MacLane's book's great"
date: 2015-03-05 09:34:33 +0100
comments: true
published: false
categories: ["Things I don't yet understand", "Category theory"]
---

Since years, I am studying category theory on and off, for its applications to
programming. After reading parts of Pierce, Barr and Wells and Awodey, I
recently approaches MacLane's famous textbook, and I finally started getting why
every mathematician recommends MacLane, and why no book for non-mathematicians
is like it.

Caveat: I read a lot about mathematics, but I'm not formally trained in it. So
what follows might be hard-to-follow

> Mathematics provides for more compelling, and even concrete examples.

When applying category theory to functional programming, how many really
different categories do we have? In the end, it often all boils down to the
semantics of programs. If you're lucky, maybe you deal with syntax in the
category of substitutions.

Instead, take solids with holes. You can study paths from a base point through
these holes, identify them if they can be deformed into each other, and allow
composing them or inverting them---this way, you get the
[*fundamental group*](https://en.wikipedia.org/wiki/Fundamental_group). This
construction has multiple applications

> He does not hide definitions away.

Adjoint functors are motivated and exemplified already in the introduction.
