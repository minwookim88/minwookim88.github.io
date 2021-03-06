---
layout: posts
title:  "Probability Space"
date:   2019-08-31 20:00:00 -0700
categories:
  - Math
  - Probability_Theory
---
<b>Probability space</b> is a mathematical construct that defines the notion of event and probability in a formal way. It is a special subclass of a measure space, a more general concept that defines measure (e.g. length, area, volume) and measurable objects (e.g. line, rectangle, sphere) mathematically.

<b>A measure space</b> is identified by triple
$(X, \mathcal{A}, \mu)$, where $X$ is a set of elements, $\mathcal{A}$ (called <b>$\boldsymbol{\sigma}-$algebra</b>) is a set of measurable objects that are made up of the elements of $X$ , and $\mu$ (called <b>measure</b>) is a quantitative measurement function that estimates the dimension of these objects in $\mathcal{A}$ . A familiar example would be $(\mathbb{R}, \mathcal{L}, \lambda^{(1)})$. In this measure space, the interval $[3,4] \in \mathcal{L}$ (called <b>Lebesgue $\boldsymbol{\sigma}-$algebra</b>), a length-measurable object composed of elements $x$ in $\mathbb{R}$, is measured by length measurement function $\lambda^{(1)}$ (called <b>Lebesgue measure</b>), giving $\lambda^{(1)}([3,4])=4-3=1$. Similarly, 2-dimensional counterpart $(\mathbb{R}^2, \mathcal{L}, \lambda^{(2)})$ gives area-measurable space. For example, the measure of the rectangle $[2,5]\times[-3,7]$ is given by $\lambda^{(2)}([2,5]\times[-3,7])$ $= (5-2)\times(7-(-3))=30$.

As a subclass of measure space, probability space in itself is also a measure space uniquely identified by triple $(\Omega, \mathcal{F}, P)$, with domain-specific notation (but meaning is the same). A measure space is called <b>Probability space</b> if the measure function satisfies the following properties (called <b>Kolmogorov Axioms</b>):
<ol style="list-style-type:none">
  <li> <i>Nonnegativity</i>: For any measurable object $A \in \mathcal{A}$, &nbsp;&nbsp;$\mu(A)\ge0$. </li>
  <li> <i>Finite measure</i>: Measure of the entire space is finite (or equal to 1 up to a constant factor). That is,&nbsp;&nbsp;$\mu(X)=1$.</li>
  <li> <i>$\sigma-$additivity</i>: For any countably many set of measurable objects $\{A_i\}_{i\ge1}$ that are mutually exclusive (i.e. $A_i \cap A_j = \varnothing$ for $i\neq j$),
&nbsp;&nbsp;$\mu\left(\bigcup\limits_{i=1}^\infty A_i \right) = \sum\limits_{i=1}^\infty \mu(A_i)$.
</li>
</ol>

. Specifically for probability space, we use $(\Omega, \mathcal{F}, P)$ notation, where
$\Omega$ denotes <b>sample space</b>, $\mathcal{F}$ denotes <b>event space</b>,
and $P$ denotes <b>probability function</b>(measure). 

Probability space is a mathematical system that is specifically designed to describe event and probability. Suppose there is a random-number generator that [uniformly]({% post_url 2020-03-05-Distribution (3) Uniform %}) spits out any real number $x\in\mathbb{R}$ drawn from the interval $[0,1]$. In this case,

<ol>
  <li><b>Sample space</b>($\Omega$): The closed interval $[0,1]$ is the sample space which is composed of atomic elements (=real numbers) that are smallest probability-measurable objects. Sample space is supposed to represent the set of all potential outcomes that could result from
<a href="{% link _posts/2019-05-07-Data Encodes Information.md %}">
the observation we are trying to make for any unobserved scene in pursuit of evidence of truth
</a>.
  </li>
  <li><b>Event</b>($E\in\mathcal{F}$): Any (probability-measurable) bundles or sets of these atomic outcomes such as $A=[0.2,0.35)$, $B=(0.1,0.2]\cup[0.8,1]$ are called <b>events</b>, each of which is a member of <b>event space</b>. Events are designed to represent <i>groups</i> of atomic outcomes that one might be more interested in than individual outcome. The choice of this grouping schema determines the very nature of events and reflects one's 
<a href="{% link _posts/2019-09-14-Random Variable and Distribution.md %}">
true interests in observation, which is directly associated with random variable
</a>.
  </li>
<figure>
  <img src="/assets/images/sample_space.png">
</figure>
  <li><b>Probability measure</b>($P$): Because atomic outcomes occur uniformly, the corresponding atomic events are equally likely to happen. In this case, the <b>probability measure</b> on events happens to be equal to Lebesgue measure on the same topological sets, which gives $P(A) = 0.15$ and $P(B)=0.3$.
Probability measure is supposed to measure the likelihood amount of a given
events (=probability-measurable objects).
  </li>
</ol>

A more familiar example would be rolling a dice. With a standard die of regular hexagon shape, $\Omega =${$1,2,3,4,5,6$}. Then, any set $A$ made up of the atomic elements of $\Omega$ is probability-measurable and thus called event. For example, the event of observing any odd number is defined by $O=${$1,3,5$}, and its probability is given by $P(O)=0.5$. More specifically, the actual computation of the probability comes from the following two facts: 

<ul>
  <li> Each atomic event is equally probable; that is, <br> $P(${$1$}$)=P(${$2$}$)=\cdots=P(${$6$}$)=1/6$. <br>This is thought to be true if,
    <ol style="list-style-type:none">
      <li> The die has equal area for each facet.</li>
      <li>The center of mass agrees with the geometric center.</li>
      <li>The dice roller has no biased trick that affects likelihood of the result of roll.</li>
    </ol>
  </li>
  <li> Each atomic event {$1$},{$3$},{$5$} that constitutes the event $O$ of interest is mutually exclusive.
  </li>
</ul>

So, from the above facts and $\sigma-$additivity of the probability measure, we have
$P(A)=P(${$1$}$)+P(${$3$}$)+P(${$5$}$)=3/6=0.5$.

In summary, probability space is a mathematical construct that describes event and probability. It is this formal definition of the construct that enables us to quantitatively define and measure uncertainty of events (=probability-measurable objects) that we are modeling by means of probability function, which is designed to measure the quantitative amount of certainty/uncertainty of events. Upon the foundation of such solid definition, probability measure holds various properties that prove to be useful in computing probability, including

<ul>
  <li>$P(\varnothing)=0$.</li>
  <li>For disjoint events $\{A_i\}$, $P(\bigcup\limits_{i=1}^nA_i)=\sum\limits_{i=1}^nP(A_i)$</li>
  <li>$P(A^c)=1-P(A)$.</li>
  <li>$P(A\cup B)=P(A)+P(B)-P(A\cap B)$.</li>  
</ul>

. More detailed discussion on probability, distribution and its computation continues on [this post]({% post_url 2019-09-14-Random Variable and Distribution %}).