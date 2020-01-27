---
layout: post
title:  A New Mental Model for Data Science Programs
tags:
- data science
- software engineering
categories:
- hdsk
---

Mental models (abstractions, metaphors, patterns, etc.) play a
critical role in our understanding of reality, especially in
software. You might even make the case that a mental model _is_ our
understanding.

In this post, I propose a (potentially) new mental model for
reasoning about data science programs which I think enables a more
intuitive understanding of the mapping between the program's code and
the underlying mathematical concepts. I think it has the potential to
support more efficient workflows for practitioners and a friendlier
learning experience for new-comers.

<!-- MORE -->

But first, a little exposition on what I mean by "mental model" when
it comes to software:

One common way we mentally represent software is as a state machine.
This is, historically, has been a pretty good model that maps well to
the physical operation of a computing machine; at any particular
moment, the registers in the CPU collectively have a particular
state, and the next instruction describes how to transition to the
next state. At a slightly higher level, we can represent the state of
a program as a particular piece of data, and the functions and
methods in the program dictate how to transition. This, historically,
has also been an appropriate use of the state machine model, as it
maps closely to the state and behavior of objects in an OOP program.

Another model for software is that of a pipeline, or more
specifically, a data transformation pipeline. We can view computation
as the act of applying sequential transformations to a piece of data
until it communicates the desired information. Each step is like a
segment of pipe that we can affix to the pipeline we already have.
For example, this plays out in a very literal sense in the
construction of UNIX pipelines, and in a less literal sense in the
Map-Reduce paradigm and in the composition of functions in a
functional programming language.

<pre><code class="shell">$ ps aux | grep $(whoami) | tr -d $HOME
</code></pre>

I also think this model maps well to the practice of data science. We
start with some input data and meticulously compose a sequence of
steps to reach some mathematical conclusion or insight.

This alone isn't new; we often talk about "the data science pipeline"
(it's often an ambiguous phrase, but it shows this model is present
in the community's collective consciousness).

The weakness of this model for data science is that it doesn't offer
a clear socket where we can "plug in" domain knowledge (in this case,
mathematical facts about the algorithms we're applying to the data).
Basic type checking introduces a notion of validity for different
combinations of pipe segments, but doesn't give us the language to
express those mathematical facts. They live in a separate reality and
must be reasoned about separately from the program.

Let's step back and inspect the process to see what useful metaphors
we might derive.

We start with a hypothesis about some data, which we set out to test
using some algorithm(s). However, these algorithms are very
particular about the properties of their input data, and the data we
have right now is big and messy. It's our job to massage the data on
hand until it has the properties required of it by the algorithm.
This can mean normalizing, handling missing values, ensuring a
particular class balance, anything.

Many popular libraries document these requirements in prose and stop
there. In fact, it's generous to even call them "requirements"
because the runtime will happily apply those algorithms to data which
doesn't meet the preconditions. It says "I trust that you made sure
these conditions hold." The tooling does nothing to help out the
practitioner who forgot a step or the novice who didn't know about
it.

I think our libraries should instead require us to present evidence
for the required properties. The API should be a gatekeeper which
expects a particular tax before permitting entry. ID3 decision trees
don't handle missing values, so we should present to it a proof that
the data is free of them. KMeans can give unexpected results for
unnormalized data, so we should present to it proof that the data is
normal (or explicitly state that we are aware the data is irregular
and want to cluster anyway). Neural networks expect input tensors of
a particular shape, so we should present to them proof that the input
data does in fact have that shape.

By being aware of the properties of our data required by our
algorithms, and explicit with the evidence of those properties, we
intrinsically tie facts about the underlying mathematics to the
program and to our internal mental model of it. Furthermore, when the
program's runtime or compiler is _also_ aware of those properties, it
can become an invaluable tool for both engineering and instruction.
Equipped with such domain knowledge, a type checker could, for
example, detect when evidence of normality has been omitted for
clustering and explain why it is needed, teaching the user something
about clustering. It can also support more efficient error reporting,
making the debugging process much faster and more convenient.

In the last few posts, I've explored the meaning of "correctness" as
it applies to data science software, and I think this is a good
summary of my findings so far. Data science algorithms all have a
gatekeeper which prohibit entry until a sufficient tax has been paid
in evidence.
