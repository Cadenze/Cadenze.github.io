---
layout: post
title: The Torture Symbol
---

This year we will be pivoting towards new mathematical ideas.

## Introduction

In this article we will construct and define the torture symbol,
which we will show plays an important part in real analysis,
and extends well beyond what we will discuss here,
with plenty of applications outside the field of mathematics.

## Definition

We first define a 'mutilation' $\mathcal{M}$ on a (real) interval.
This is the act of splitting an interval into finitely many parts.
Suppose we have a bounded function $f:[a,b] \to \mathbb{R}$.
We denote the supremum and the infimum on each of the mutilated parts
as $M_i = \sup\{f(x): x \in [x_{i-1},x_i]\}$
and $m_i = \inf\{f(x): x \in [x_{i-1},x_i]\}$ respectively.
We can now coerce the function to add up all its mutilated parts
and define $U(\mathcal{M},f) = \sum_{i=1}^n M_i \Delta x_i$
and $L(\mathcal{M},f) = \sum_{i=1}^n m_i \Delta x_i$.

If we now attempt to torture each of these sums,
we can define $T_U(f) = \inf U(f)$ and $T_L(f) = \sup L(f)$,
where the infimum and supremum are taken
over all possible mutilations of our interval $[a,b]$.
If these two torture methods equate to each other,
we now say that the torture is successful,
and we denote that value as $T(f)$ or $T_a^b(f)$
if we want to emphasize that we are torturing the function over a specific interval.

## Some Specific Results

In order to prove some results,
we will first define one more thing.
The supermutilation is defined as cutting up an original mutilation into more parts.
Notice that the supermutilation must have the same cuts as the original one.
A common supermutilation is defined to be the mutilation
that has exactly the cuts of two other mutilations.

We claim that for any function,
$T_L(f) \leq T_U(f)$.
Suppose we have two arbitrary mutilations $\mathcal{M}_1$ and $\mathcal{M}_2$.
Let $\mathcal{M}^\star$ be the common supermutilation.
We can see it is obvious that
$L(\mathcal{M}_1,f) \leq L(\mathcal{M}^\star,f)
\leq U(\mathcal{M}^\star,f) \leq U(\mathcal{M}_2,f)$,
so in particular, $\sup L(\mathcal{M},f) \leq U(\mathcal{M}_2,f)$,
and hence $\sup L(\mathcal{M},f) \leq \inf U(\mathcal{M},f)$,
which is exactly our definition for the torture methods.

The following theorem gives a criterion on the torturability of a function.
We claim that a function is torturable if and only if
there always exists a mutilation that allows $U$ and $L$ to be arbitrarily close.
If a function is torturable,
then we know $\sup L(\mathcal{M}) = \inf U(\mathcal{M})$.
For any $\epsilon > 0$,
we can find a mutilation $\mathcal{M}_1$
such that $T(f) - L(\mathcal{M}_1) < \epsilon/2$,
and similarly we can find another mutilation $\mathcal{M}_2$
such that $U(\mathcal{M}_2) - T(f) < \epsilon/2$.
Then it is easy to see that the common supermutilation $\mathcal{M}^\star$
must be $U(\mathcal{M}^\star) - L(\mathcal{M}^\star)
\leq U(\mathcal{M}_2) - L(\mathcal{M}_1) < \epsilon/2 + \epsilon/2 = \epsilon$
as desired.
For the reverse direction,
we know that $0 \leq T_U(f) - T_L(f) \leq U(\mathcal{M}) - L(\mathcal{M}) < \epsilon$.
Since the choice of $\epsilon$ is arbitrary,
$T_U(f) - T_L(f) = 0$ and they must be equal.

## A Few Exercises for the Reader

We will leave the linearity of the torture symbol
and some other properties as an exercise for the reader.
Nevertheless, we will formally state them here.

1. $T(f_1 + f_2) = T(f_1) + T(f_2)$.
2. $T(cf) = cT(f)$.
3. $f_1 \leq f_2 \implies T(f_1) \leq T(f_2)$.
4. $T_a^b(f) = T_a^c(f) + T_c^b(f)$.
5. $|f| \leq M \implies \left|T_a^b(f)\right| \leq M(b-a)$

## The Deep Connection

We will now demonstrate that the torture symbol
is deeply linked to other parts of analysis,
in particular a concept that is usually taught early on in calculus.
This will be presented in two so called 'fundamental theorems'.

The first fundamental theorem states that
suppose $F(x) = T_a^x(f)$.
Then $F$ will be continuous,
and if $f$ is also continuous at some point $x_0$,
then $F$ is also differentiable at that point,
with $F'(x_0) = f(x_0)$.
We first prove continuity.
Since $f$ is torturable,
it is bounded for some $|f| \leq M$.
Let $|y-x| < \delta = \epsilon/M$.
For $a \leq x \leq y \leq b$,
it is easy to see that
$|F(y) - F(x)| = |T_a^y(f) - T_a^x(f)| = |T_x^y(f)| \leq M|y-x| < M\delta = \epsilon$.
We now prove differentiability.
For $h > 0$,
$\frac{1}{h}[F(x_0+h)-F(x_0)]-f(x_0)
= \frac{1}{h}T_{x_0}^{x_0+h}(f) - f(x_0) = \frac{1}{h}T_{x_0}^{x_0+h}(f-f(x_0))$.
By continuity of $f$,
we can always find a $\delta$ such that
$|t-x_0| < \delta \implies |f(t)-f(x_0)| < \epsilon$.
Let $h < \delta$.
Then $|\frac{1}{h}[F(x_0+h)-F(x_0)]-f(x_0)| \leq \frac{1}{h}T_{x_0}^{x_0+h}(|f-f(x_0)|)
< \frac{1}{h}\epsilon h = \epsilon$.

The second such theorem states that
if there exists a differentiable $F$ such that $F' = f$ torturable,
then $T_a^b(f) = F(b) - F(a)$.
Indeed, for any mutilation, $F(b) - F(a) = \sum_{i=1}^n [F(x_i)-F(x_{i-1})]$.
By the very familiar mean value theorem,
we can find some $t_i$ between our two $x$ such that
$F(b) - F(a) = \sum_{i=1}^n F'(t_i) \Delta x_i = \sum_{i=1}^n f(t_i) \Delta x_i$,
and this value is definitely between $L$ and $U$.
Also we notice that $T_a^b(f)$ is also bounded by $L$ and $U$.
By taking $L$ and $U$ arbitrarily close to each other,
we can see that $F(b) - F(a) = T_a^b(f)$ eventually.

We can now clearly see that this coincides exactly
with the fundamental theorems of calculus.
Hence we conclude that
the torture symbol can be written as $T_a^b(f) = \int_a^b f \, dx$.

## Acknowledgements

I know I'm too busy this year to write up an actual April's Fools post,
so I had to borrow material from known sources.
In any case,
I would like attribute the material to (the torture inflicted on me by)
Walter Rudin's 'Principles of Mathematical Analysis' Chapter 6,
in particular Definitions 6.1 and 6.3,
and Theorems 6.5, 6.6, 6.12, 6.20, and 6,21;
and of course by extension to the 3rd year real analysis courses at UBC.
Furthermore, a big thank you to Madeline Forbes
for providing inspiration and coining the term 'torture symbol'.
