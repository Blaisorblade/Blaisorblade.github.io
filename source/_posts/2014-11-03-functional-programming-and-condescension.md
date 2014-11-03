---
layout: post
title: "Functional programming and condescension"
date: 2014-11-03 15:18:16 +0100
comments: true
published: false
categories: [Community]
---

I love statically typed functional programming, but many people disparage who disagrees, and nobody is entitled to do that. The superiority of some programming languages, unfortunately, is not scientific fact but "religion"; we can subscribe to one religion, but we must be tolerant of others. We can have intelligent debates over language design, but what is better is always conditional on some (implicit) assumptions.

<!-- more -->

> I love functional programming & types, but nobody is entitled to insult who disagrees. I am studying for a PhD in programming languages, and I have strong opinions on what languages I prefer to use, but I can tell you that the superiority of any programming language is not scientific certainty, but "religion"; we can subscribe to such "religions" (and I do), but talking about the one true "religion" is fundamentalism. Hence, as a functional programmer talking to other functional programmers, I will say that the condescension some of you have is not justified. In fact, many (but not all) programming language researchers carefully avoid treating the superiority of a language as fact.

The rest of this blog post is going to explain and argue for the above paragraph. I'm going to "explain" it because, among other things, I'm using both "religion" and "scientific fact" in specific (or peculiar) ways.

What's "scientific certainty"? My mind is wired like a mathematician, so I can be very restrictive there. "2 + 2 = 4 (if you buy some axioms of mathematics & all the definitions being used)" is a fact. The laws of physics are the best known way to explain the universe — physicists don't treat them as absolute certainties when they investigate the ultimate foundations of the universe. But in the context of everyday life, they're scientific certainty.

So:
- 2 + 2 = 5 is *wrong*;
- building a bridge based on some alternative physics (say, Aristotelian physics) is *wrong*;
- using the wrong tools to build a bridge is most probably a bad idea. XXX add example.

As you see, before telling somebody he's wrong, I require pretty strong arguments.

Now, back to programming languages. Some people could say that:
1. using a "bad" programming language for a job resembles using the wrong tools; or maybe, that it resembles using Aristotelian physics to build a bridge;
2. for certain reasons, language X is "bad" and language Y is "good".

However, how do we know when a programming language is "good" or "bad"? Most of the time, we can argue a lot about that, but we don't know.

Here are a few things I will assume without much discussion for the sake of brevity; some of them I have learned, as a PhD student in programming languages.

- not all programming languages are designed equal. C is not memory-safe, and this allows lots of security vulnerabilities which would not be possible in safe languages.
- if some programmers produces bad code for their job, and their job is useful for society, they're arguably a drain on society, because of the maintenance cost it will impose on you and other programmers.
- nowadays, we don't have a scientific way to evaluate designs in general; at best, we can discuss some technical tradeoffs, but in many cases we have no scientific way to judge the value
- when we 

However,
- the programming language is just one (very important) part of the software engineering process. Verification technologies other than type systems exist. Some C software are proven safe with other technologies, and scientists do not agree whether 

; if you use C (especially the traditional C string functions) for parsing strings in a mission-critical system, you will need extra complexity elsewhere in code reviewing or verification technology


Here are some facts about static typing, both positive and negative:
- using types you can prevent some errors statically, and in languages with expressive type systems you can turn more possible mistakes into static errors. That's a mathematical certainty.
- every type system will reject some correct programs because it is not expressive enough. That's also a mathematical certainty.
- there are ways to abstract over code that are more difficult to treat with static type systems — there are many elegant ways to do that, but this is a topic of ongoing research.

Now, if we agree on which properties are more important, 

However, 

Here are some value judgements about types:
- it's better to statically reject wrong programs than 
- while 

Here are a value judgement about types:
- using statically typed languages is the only true way to write software

In some contexts (such as mission-critical software)

Historically, I conjecture the culture of condescension 
