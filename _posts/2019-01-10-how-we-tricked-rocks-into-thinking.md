---
title:  How We Tricked Rocks Into Thinking
layout: post
tags:
  - computers
  - hardware
categories:
  - thinking-rocks
---

Computers are fundamentally little more than chunks of metal,
plastic, and semi-conductive material. How do collections of such
simple molecules give rise to the breathtaking CGI space-scapes of
*Interstellar*, the vast and omnipresent Internet, and the shrewd,
[alien<i class="fa fa-external-link"></i>][wired]{:target="_blank"}
strategy invented by *AlphaGo*?

[wired]: https://www.wired.com/2016/03/sadness-beauty-watching-googles-ai-play-go

<!-- MORE -->

![Interstellar Black
Hole](https://thefilmstage.com/wp-content/uploads/2014/10/interstellar_blackhole.png)
{% include caption.html
    text="The most accurate rendering of a black hole ever"
    href="https://thefilmstage.com/news/how-interstellar-creates-the-universes-most-accurate-simulation-of-a-black-hole" %}

This short essay series is an attempt to dramatically oversimplify
the answer to that question by consolidating the teachings of Logic
Design, Computer Architecture, and Operating Systems into an
accessible narrative.

Title inspired by [this<i class="fa
fa-external-link"></i>][twitter]{:target="_blank"} tweet.

[twitter]: https://twitter.com/daisyowl/status/841802094361235456

## Roadmap

We're going to be making this journey one step at a time, and taking
those steps in order; each successive concept will build off the
previous ones.

We'll start with a quick survey of computing technology through the
ages. When we reach the 19th century, we're going to slow down and
dip our toes into the murky waters of Logic Design and explore
**why** digital computers don't have to be electrical gadgets. With
that in mind, we're going to design a simple calculator.

Once we've tried our hand at designing a digital system, we're going
to look at the paradigm behind modern, "general purpose" computers,
and at how and why it works. Using that as a guide, we'll crack open
a microprocessor to see what's inside.

By then, we'll be able to start picking apart the massive web of code
that is an operating system and hopefully understand what makes our
computers tick, and how we go from code to real world actions and
consequences.
