---
layout: post
title: "Turning type constructors into functors through Kan extensions"
date: 2016-02-14 22:18:58 +0100
comments: true
categories: ["Category theory"]
published: false
---

Often, when applying category theory to advanced programming languages, people
take some construction that requires functors, and apply to type constructors
that are not functors. That always left me confused.

For instance, to build the
[*freer monad*](http://okmij.org/ftp/Computation/free-monad.html), Oleg Kiselyov
and Hiromi Ishii apply the *left Kan extension* (which works on functors) to
something that is not a functor.

Elsewhere, people do the same thing, but call it Coyoneda:
http://underscore.io/blog/posts/2015/04/14/free-monads-are-simple.html
http://typelevel.org/blog/2014/06/22/mapping-sets.html

Thankfully, my colleague Cai Yufei explained what was going on.

While a Haskell/Scala functor is an endofunctor in the category of types and
functions of the language, a type constructor is still a functor, but from a
different category: the *discrete* category of types.

Let's dive in to understand what is going on.

# The discrete category, and functors on it

A discrete category has no arrows except for identity arrows. Composition also
becomes trivial, since identity arrows can only be composed with identity
arrows.
