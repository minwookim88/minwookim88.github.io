---
layout: posts
title:  "Probability Space"
date:   2020-03-30 20:00:00 -0700
categories:
  - Math
  - Stat
---
<b>Probability space</b> is a mathematical construct that defines the notion of event and probability in a formal way. It is a special subclass of a measure space, a more general concept that defines measure (e.g. length, area, volume) and measurable objects (e.g. line, rectangle, sphere) mathematically.

<b>A measure space</b> is identified by triple
$(X, \mathcal{A}, \mu)$, where $X$ is a set of elements, $\mathcal{A}$ (called <b>$\boldsymbol{\sigma}-$algebra</b>) is a set of measurable objects that are made up of the elements in $X$ , and $\mu$ (called <b>measure</b>) is a quantitative measurement function that estimates the dimension of these objects in $\mathcal{A}$ . A familiar example would be $(\mathbb{R}, \mathcal{L}, \lambda^{(1)})$. In this measure space, the interval $[3,4] \in \mathcal{L}$ (called <b>Lebesgue $\boldsymbol{\sigma}-$algebra</b>), a length-measurable object composed of elements $x$ in $X$, is measured by length measurement function $\lambda^{(1)}$ (called <b>Lebesgue measure</b>), giving $\lambda^{(1)}([3,4])=4-3=1$. Similarly, 2-dimensional counterpart $(\mathbb{R}^2, \mathcal{L}, \lambda^{(2)})$ gives area-measurable space.

As a subclass of measure space, probability space in itself is also a measure space identified triple $(\Omega, \mathcal{F}, P)$.

So, the $P$ notation we typically see is a symbol that denotes an actual mathematical function that measures probability of events; not a mere nominal symbol. That means, the function is subject to mathematical manipulation such as differentiation, integration, and limit. 
