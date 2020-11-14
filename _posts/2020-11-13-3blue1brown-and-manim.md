---
layout: post
title: 3Blue1Brown and Manim
---

Well, certainly I have finally got the time to write something.

Grant Sanderson, otherwise known as 3Blue1Brown, is a Youtuber that posts videos about mathematics. If you haven't seen any of his work, do check out his [website](https://www.3blue1brown.com) and [channel](https://www.youtube.com/c/3blue1brown).

For those who have watched 3Blue1Brown videos, you will know how he presents math concepts: with the use of very clean animations. Well, today's topic isn't about his channel, it's about the animations.

## Visualizing Mathematics

More often than not, mathematics requires a lot of formulae and graphs, and sometimes those things change over time; there's even an entire field of math dedicated to studying change. Static figures often don't do justice to these concepts, and with the widespread usage of computer screens, it seems counterintuitive to try understanding mathematics only through textbooks.

This problem was exactly what I encountered when trying to summarize Perelman's proof of the Poincaré in 1250 words. Diagrams are very important and useful, but do they translate well if I were to present to an audience? Is there a better medium?

## Mathematics Animation Engine

There is apparently a way to present mathematical concepts in the way 3Blue1Brown does it. In fact, the engine that he developed for his videos is available on [GitHub](https://github.com/3b1b/manim). There even is a [community-maintained version](https://docs.manim.community/en/latest/index.html), which I have been told, is updated more regularly.

The engine differs from traditional animation engines in the sense that it is mathematics first, animation second. With Manim, you can create accurate graphs and objects, and paths are easily tracked and traced. Everything is mathematically defined, and therefore it is more convenient to scientific animations than vector drawing software, where every endpoint, every curve has to be tweaked and adjusted.

However, there are downsides, the biggest of which is that **Manim does not have a user interface**. It is a very powerful tool, yet it is not user-friendly at all. The user has to manually write code in Python, run sections of it on a terminal, before obtaining a single piece of animated math. For those who are not familiar with computer science, you will most likely have to learn the syntax of Python, the lexicon of Manim, and how to translate math into code (i.e. the formatting of LaTeX).

On the other hand, as a user with about a year of experience in Python and Java each, Manim was relatively easy to pick up once you understood its strengths and limitations, despite being as convoluted and complicated as it can be. Next time if you ever think about doing a math/science project, don't hesitate to try using Manim to make your presentation look sleek as hell.

If you want to take a look at my animations, I have made a [PowerPoint](/files/resources/Poincare-Conjecture.pptx) containing all of them. To see the code that made these animations, head over to my [GitHub here](https://github.com/Cadenze/t1-poincare).