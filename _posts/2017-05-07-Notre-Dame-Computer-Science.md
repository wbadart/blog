---
title: Notre Dame Computer Science
tags:
  - computer science
  - education
  - notre dame
date: 2017-05-07 03:10:19
categories:
  - ethics
layout: post
---


Episode two of the Ethics in Computing Podcast is a discussion of the Notre Dame Computer Science program. Please find the audio and transcript below.

<!-- MORE -->

But first, for my non-Notre Dame readers out there, here's a little background for the clip you're about to hear:
When you first become a domer, you have no major, and are in the same college as all 2,000 of your classmates: [First Year of Studies](https://firstyear.nd.edu). What you do have is an *intended college* (and, if you're one of a lucky few, an intended major). The fledgling engineers, rather than taking *Intro to Chemical Engineering* or *Fundamentals of Computing*, take a two semester series in "Engineering." It's like a dim sum restaurant of engineering disciplines, structured around a few projects that focus on one field or another. This class is a trade-off for our engineers: those freshmen who stick with engineering are given a broad (if cursory) introduction to engineering concepts (and MATLAB), but it comes at the cost of being a semester or even a year behind peers at other universities who may have been diving into major material from day one.

<iframe src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/321980771&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;visual=true"></iframe>

I'm sure I've mentioned before that I think the first year engineering program was one of the most important parts of my education at Notre Dame. It's easy to fall into the trap of speculating how much farther ahead you'd have been without the program; I've done it myself. In reality though, I've observed that we as a class of computer scientists are **passionate** and **competitive** (sometimes competitive with one another but mostly in the sense that we often do more than just stand our ground against CSers from other universities).

For me, as someone who (as a freshman) wasn't just unsure if I wanted CS but as someone who wasn't sure if I wanted engineering at all, Intro to Engineering put my doubts to rest. By Spring's end, with the [MATLAB project](https://github.com/wbadart/Project-Holmes) under my belt, I knew CS was going to be my jam, and I know at least a couple other people who had the same reaction.

(Brief aside: I know my experience, that of a single individual, can't be the sole argument for the value of the first year engineering program. All I mean to do is present the potential impact that the program can have on at least some of its individual participants.)

![](/assets/images/matlab.png){:width="400"}

Sophomore year was a strong follow up to the post-MATLAB glow. I'm glad we were taught C for Fundamentals of Computing I: C in general doesn't hold your hand, so it's harder to fudge things. Also, [C-like syntax](https://en.wikipedia.org/wiki/List_of_C-family_programming_languages) is everywhere, so having that language as our base set us up for fluency in a multitude of other languages. There are definitely disadvantages to starting with C, chief among which is (in my opinion) a hard-wiring towards imperative programming which must often be unlearned (or at least reduced) at some point down the line. Last summer, after making a concerted effort to write more modular and functional code for Booz Allen, my code quality and the efficiency of the application grew enormously.

And then there was Verilog.

I had some mixed feelings about Verilog while taking Computer Architecture, but in hindsight, I'm glad I learned it. Verilog, under Dr. Brockman's skilled instruction, helped demystify the internals of transistor-based computer components (which I think is essential for all CSEs). Not to mention, Verilog (along with MIPS) were highlights of my [technical discussions](https://blog.wbadart.info/2017/01/30/The-Blind-Leading-the-Blind/) with NSA recruiters (thanks Dr. Brockman!) last fall. Finally, I can't help but notice, looking back, the similarities between the flow of signals through sequential logic in Verilog and the treatment or flow of data through functional programs (the program is [the pipeline](https://en.wikipedia.org/wiki/Pipeline_programming#Other_considerations)).

Discrete math was also cool, but a little *extra* at times. It might have worked better as a tech elective for the more mathematically minded in our class. In theory, it's a stepping stone to Theory, but I feel like the discrete concepts referenced in Theory were so fundamental, they hardly needed a whole course's worth of treatment beforehand. I know I was going in a nice chronological order with the classes, but since we're talking about it, here are my two cents on theory: it's a fantastic class that teaches things you might not think will be relevant to your career, but will undoubtedly become so at some point or another. Constructing a Turing machine to detect strings with XYZ random properties is certainly dull and arbitrary at the time, but a strong understanding of state machines will take you far in video game development, web apps, or pretty much anything else where a stream of data dictates the application state at a given moment. I say keep that class right where it is.

This came up the other day in class: Fund. Comp. II gave us just enough C++ to understand how powerful it is, and not nearly enough to start to truly leverage that power. Instead, we got a bunch of lectures on software engineering buzzwords shoehorned into the last several weeks of the semester. I can't say first hand how the curriculum restructuring has affected this class, but from what I understand, it's been changed for the better.

The last major class of note sophomore year was Unix. I'll try not to fanboy too hard, but seriously man, this class is where it's at. With other classes, you take away maybe 20 to an optimistic 50 percent of the material and really use it. I think that number was darn near 100 for Unix. +30k.

![](/assets/images/nix.png)

In junior year, our paths as a class began to diverge as study abroad shuffled courses between our semesters. I took DS, Comp Arch, and Theory in the Fall (plus a couple electives) and Paradigms, OS, and Ethics (sup) in the Spring (plus electives/ prob stats). I really can't complain about any of these courses: I feel like I've been getting good learning from them. I'd only mention that I think Paradigms has the potential to be much more than it was; we got great breadth, but at cost of any real depth.

I'd cut out most of the frills (regex, Android, x86, cherrypy, ...) and lay it on way thicker with the Scheme/FP. And you know it doesn't even have to be Scheme: I think we could have had some very effective FP lessons in Javascript. Show us map/filter/reduce! Show us binding and partial application! Functions as first class objects! Closures (just maybe without the lambda calculus)! Those things all sound exotic from a C/imperative perspective, but they're just your average Tuesday in JS. I think a deeper dive into FP in JS could have given the class a better understanding of the benefits and relevance of FP, instead of leaving many with the nagging feeling of not having learned anything for the "real world." I'd like to add that event-driven programming is a snap in JS; it's hard to get more explicit than `window.onresize = function(){..` or `$('button').on('click', do_stuff)`. You can tie that in to the Go stuff and suddenly, you've got an awesome final project: a full-stack web application that explores FP and event-driven programming in the front end and imperative and concurrent programming in the back. I guess the stack misses any real opportunity for OOP, but I think a lot of us had more than our fill of that from Data Structures.

For all its quirks and growing pains, I **love** Notre Dame CSE -- the program guided me to my passion and set me up with a bright future full of learning and opportunity. I'm grateful to the faculty who work tirelessly for me and my classmates as we prepare to graduate (be it in twelve days or twelve months) and make our marks on the world.

W


