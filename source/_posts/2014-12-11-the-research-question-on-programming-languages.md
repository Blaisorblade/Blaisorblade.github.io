---
layout: post
title: "Programming language research for laypeople"
date: 2014-12-11 01:25:30 +0100
comments: true
published: false
categories: research meta
---

What's programming language (PL) research? Is it relevant? Why? Are researchers
asking the right questions? Is this field a science? Should you care as a
programmer? And if you are a layperson?

To judge PL research you need answers to these questions. And if you design
software, your design decisions are often grounded in some assumptions on how to
best program --- but many of those assumptions, down to the notations you use to
write programs, are still object of research, also because the field is so
young.

To gain some perspective, imagine that engineers still needed to do research on
how to best do technical drawings while designing a rocket for Mars, or that
mathematicians did research on how to write numbers on paper while having to do
advanced mathematics. Imagine further that there's a "religion war" between
different positions on these topics, because nobody can quite figure how to make
a decision, and that beginners learn different notations in universities
depending on the professors they run into.

In fact, such debates also affect you because, when you write a program, you are
continuously extending the notation─the language─by creating new program pieces
you can use in the rest of the program.

To answer, I'll first explain PL research for laypeople.

In future posts, I'll deal with the other questions. In the end, I'll explain
why the crucial questions are barely entering the domain of science. As a
corollary, we'll learn why PL discussions (at least outside of academic venues)
often become religion wars, and why such fundamentalist attitudes to PLs are
anti-scientific.

(You might question the very idea of relating such different questions. )

In this post, I present the general research field I work on: programming languages. While my PhD is focused on a small part of the area ([as it should be](http://matt.might.net/articles/phd-school-in-pictures/)), I think it's interesting to understand the goals of the area. Moreover, there's some debate on what researchers should do, and I'd like to contribute my two cents.

## Programming language design for laymen
Often people ask me what I work on. Often it's too hard to discuss details, but I usually try my best at providing a picture of the research . Here's what I'd answer to a non computer scientist:

While my PhD is focused on a small part of the area ([as it should be](http://matt.might.net/articles/phd-school-in-pictures/)), 

> To get computers to help us get stuff done, we need to teach them. However,
computers are great at following instructions precisely, but not so much at
figuring them out, so we need some people (called *programmers*) to write these
instructions (called *programs*) for computers and make them correct and
precise. These instructions must be correct because computers are not smart
enough to ignore wrong instructions, and they must be precise because computers
are not smart enough to guess details by themselves.
>
> To do so, programmers don't use English, because (among other reasons)
computers don't understand it, and it's not precise enough; rather, they use
artificial languages that humans designs. Designers of programming languages try
to help their users, that is programmers, to achieve their goal, that is writing
programs. Some of these languages can help or hinder the programmer, so there's
a whole science about their design; and it's in this science I do my work.

In fact, I'm lying a bit, as we will see.

# The two research questions on PL

Researchers working on programming languages have, in my opinion, two main
research questions facing them:

1. what features make a programming language good?
2. how do we achieve these features?

 many experts agree that:
- since programmers usually can't write the perfect program in one go, and need help from colleagues.

- being able to teach new concepts to computers is good
- automating tedious
- programmers don't want to repeat themselves.

My perspective on this 

==

These are very general questions, so any paper will focus on one aspect of them.
For instance, a programming language can have (or not) a static type system,
which labels some programs incorrect and rejects them.

The two questions above, specialized to type systems, become:
1. does a static type system make a programming language better?
2. how do we create a static type system?

However, we should only ask how to create a static type system if
this improves a programming language. Hence,

However, **while we know a lot on creating type systems, we know very little on
whether they help**.

## Truth in science

## PL design, philosophy and prescience

According to some PL researchers, we should evaluate programming language design
decisions by trying out empirically whether they help people achieve certain
tasks. As you might guess from the rest of the essay, I agree in principle.

However, many scholars object for various reasons. Here are the objections I
find interesting to discuss:

- a single study does not necessarily generalize. I agree, but as many have
  argue, computer science researchers need to start reproducing studies, like
  scholars.

- studies can tackle rigorously only very simple questions. We wouldn't be able
  to make a meaningful study comparing, say, functional programming to
  object-oriented programming. If we tried, the result would actually compare,
  together with the two paradigms, a lot of confounding factors:
  - specific representatives of the two paradigms (say, Haskell vs Java. Or ML
    vs Smalltalk. Would we get the same results?)
  - the syntax of the languages and its familiarity to the users
  - the educational material of the languages and the teachers

  I think this is a serious problem, which will simply require lots of patience
  to address: 

- we can't actually evaluate design ideas or research directions, but specific
  realizations, and you might evaluate a bad exemplar. For instance, suppose you
  tried to evaluate static type systems in the '60s/early '70s. At the time,
  parametric polymorphism did not exist yet. Suppose you use such a study to
  direct research on type systems: if they're not found to be effective, *of
  course* one should not do further research on them. Suppose 

    In fact, from the current evidence we can extrapolate that a study for such
    a type system would not find it useful. Stefan Hanenberg et al. XXX have
    performed ground-breaking studies on static type systems, which suggest that
    static type systems have less benefits than usually claimed. The type system
    they use is rather Java-like (without generics): in other words, it's a very
    inexpressive type system, and many modern proponents of type system would
    mention it as a bad design. (Among other things, it's not even optimal in
    any interesting dimension --- it does not have any local type inference even
    though it could support that). To be sure, such type systems are used by
    most languages, so even studying this case is important.
    
    However, I believe that testing for instance Haskell would give quite
    different results.

    Back to our thought experiment, suppose we test type systems in the '70s and
    the test indeed fails. As a consequence, Reynolds fails to get funded and
    never invents System F, so we never discover whether it's useful or not.

  some studies a design might fail not because it's a bad idea, but we
  risk evaluating a design thing, because research on . Suppose
