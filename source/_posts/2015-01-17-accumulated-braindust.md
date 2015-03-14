---
layout: post
title: "“Accumulated braindust”"
date: 2015-01-17 23:29:26 +0100
comments: true
categories: Research
published: false
---

I'm going to list (mostly research) topics/problems I have been thinking a lot about.

The title quotes
[Chris Martens](http://lambdamaphone.blogspot.it/2014/12/accumulated-braindust.html)
blog, who followed
[Conor McBride](https://pigworker.wordpress.com/2014/12/30/brains-splattered-all-over-the-walls/)
blogged a list of cool research ideas (which I hope to understand within my
life).

followed the example; while

- *Scala and ML module systems.* I've been learning about ML modules from Derek
  Dreyer's papers. That's how I understood that:

  - Scala is more inspired by ML than by Haskell in lots of ways, and lots of
    friction in the community comes from people expecting Haskell choices (even
    when they're highly debatable, see type-class coherence).
  - There's an "obvious" encoding of (some of) ML features with Scala modules,
    but it's not very well understood, also because some features have never
    been described explicitly.
    [Scala supports](http://www.cs.cmu.edu/~aldrich/courses/819/odersky-scala-theory.pdf)
    modules (through objects), signatures (through object types), functors (through classes and methods), [sharing](https://twitter.com/Blaisorblade/status/473995303100502017) [constraints](https://twitter.com/Blaisorblade/status/485435013333536768),
    though this is
    [seldom known even to experts](https://twitter.com/jonsterling/status/473994585799028736).
  - In fact, I don't know exactly what can and can't be encoded. Andreas Rossberg
    [has a long summary of the differences](http://stackoverflow.com/a/23019436/53974), but there are quite a few 
    
- *The cake pattern.* It is one of the most debated and most misunderstood
  topics in Scala development.

  - It's very powerful, because different modules can define types. However,
    it's often overkill, because in many apps modules don't define types.
  - In fact, it's just a way of using *mixin* ML modules and avoid sharing constraints.
  - As Richard Gabriel pointed out, mixins have not been designed to encode
    independent composable components, but to partition a single design into
    different slices. For starters, when you combine mixins they share a
    namespace.
  - Instead, when you need more separation, you need 
  - That's an excellent option to have, but sometimes it's really a good idea to have separate cakes.
  - The only problem is
  - However, you can also encode hierarchical modules.
  - Stateful slices are particularly painful -- they correspond to global state. Usually we would nest them via composition rather than inheritance (since 
  - As a Twitter user pointed out, stateful components shouldn't be combined in the same cake, but 
  - However, 

- Compiler writing: Why was CPS cool as an intermediate representation? Is ANF
  actually better? Or should we use yet something else?
  
  Currently, I believe the real thing is in the spectrum of modern effect
  calculi such as CBPV and System L, that use ideas in the area of linear logic
  and polarization. I learned about them thanks, among others, to Gabriel Scherer and
  Neel Krishnaswami in [this discussion](http://lambda-the-ultimate.org/node/5038).

- Incrementalization. After our PLDI'14 paper, I haven't been idle.

- Code transformations.

