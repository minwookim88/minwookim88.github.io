---
layout: posts
title:  "Random Variable and Distribution"
date:   2019-09-14 20:00:00 -0700
categories:
  - Math
  - Probability_Theory
  - Stat
  - data_science

tags:
  - random variable
  - distribution
---
<h2>Random Variable</h2>
A <b>random variable</b> is a measurable function
$X: \Omega\rightarrow E$ for a given probability space $(\Omega, \mathcal{F}, P)$
and some measure space $(E, \mathcal{A}, \mu)$.
(For the explanation of <i>probability space</i>, see
[this post]({% post_url 2019-08-31-Probability Space %});
for <i>measurable function</i>, see
<a href="https://en.wikipedia.org/wiki/Measurable_function/">this link</a>). 
From the perspective of data as being encoded information, $X$ is data encoding function that summarizes observation as per observer's interest (for the relevant discussion, see 
[this post]({% post_url 2019-05-07-Data Encodes Information %})).
Because $X$ is directly related to how observation is encoded,
the choice of $X$ depends on what types of events $\mathcal{F}$ the data collector is interested in.

Suppose we are rolling a dice. After a throw, the dice lands on a surface with certain state. The number of ways the dice can lie on a surface is infinitely many, but we are not interested in the exact status.
Because we are only interested in what the top face will be,
we choose to use a random variable function $X$ defined by <br>
$X($observation$)$=the number on the top face.

<figure>
  <img src="/assets/images/dice.png">
  <figcaption>Fig 1: Encoded data from observation</figcaption>
</figure>

After a roll, if the exact status of the dice looks like the one in the Fig 1,
we encode our observation as '6' as per the choice of our definition of random variable $X$, instead of writing verbosely like "6 on top, 4 and 3 facing toward us".
Again, this is because we are not interested in the exact status of the dice, but only intereseted in the number on top face. With this definition of $X$ as per our interest, any of the dice in the following Fig 2 is understood as being exactly the same, giving us the same data 6.
(that is, $X(w_1)=X(w_2)=X(w_3)=$$X(w_4)=X(w_5)=6$).
However, if for some reason we were interested in those 3 faces that are facing toward the dice-roller, we might have defined a new random variable $Y$ in such a way that
<ul>
<li>$Y(w_1)=Y(w_2)=(2,5,6)$</li>
<li>$Y(w_3)=(3,4,6)$</li>
<li>$Y(w_4)=(2,3,6)$</li>
<li>$Y(w_5)=(4,5,6)$</li>
</ul>
, which is a vector-valued function.

<figure>
  <img src="/assets/images/dice2.png">
  <figcaption>Fig 2:All of the dice are encoded as '6'</figcaption>
</figure>

The design choice of random variable $X$ is directly associated with and determined by type of events
(=[groups of atomic outcomes]({% post_url 2019-08-31-Probability Space%}))
that one is interested in.
Suppose we are rolling a dice. If we are only interested in whether the resulting number of the top face is even or not, we will define a function $X$ in such a way that

<ul>
<li>$X(${$1$}$)=X(${$3$}$)=X(${$5$}$)=$'odd'</li>
<li>$X(${$2$}$)=X(${$4$}$)=X(${$6$}$)=$'even'</li>
</ul>

. That is, because we are interested in observing either the 'odd' event $A:={1,3,5}$
or the 'even' event $B={2,4,6}$, we will have defined a function $X$
so that
$X(\omega)=\text{'odd'  for  } \omega \in A$ 
and $X(\omega)=\text{'even'  for  } \omega \in B$.
Then, the corresponding probability for the 'odd' event is given by <br>
$
=P(\{w \in \Omega | X(w)=\text{'odd'}\})
=P(w \in A) = P(A) = 0.5$
. Similarly, the probability for the 'even' event is $P(B)=0.5$.

In the above definition of random variable, the most common choice for set $E$ is
$n$-dimensional real space ($E=\mathbb{R}^n$, in which case $X$ gives scalar/vector-valued data)
or categorical set ($E=${$C_1,\cdots,C_n$}, in which case $X$ is category-valued).
So, each row of data that we see in data table is an encoded observation
using vector/categorical value representation.
Again, the design of data encoding mapping $X$ is solely determined by
the types of events the data collector is interested in.

<figure>
  <img src="/assets/images/random_variable.png">
  <figcaption>Random variable is data encoding mapping</figcaption>
</figure>

<h2>Probability Distribution</h2>

A <b>probability distribution (function)</b> is a function that assignes probabilities to events of interest. It is essentially same notion as probability measure, but latter is more measure-theoretic terminology, whereas the former is more statistics-specific.
However, when we say 'distribution', we are expected to discuss probabilities
in terms of random variables, whose setup is more common and realistic,
which means the types of random variables $X$ of our focus are likely to be those functions that take either
$n$-dimensional real values (i.e. $X:\Omega\rightarrow \mathbb{R}^n$)
or categorical values (i.e. $X:\Omega\rightarrow \${$C_1,\cdots,C_l$}).

Probability distribution focuses more on the resulting encoded value $x \in \mathbb{R}^n$ of $X$ than its originated individual outcomes $w \in X^{-1}(x) \subseteq \Omega$.
In this sense, probability distribution talks about probabilities in terms of values
that its associated random variable can take.
For example, suppose we are rolling a dice, and we are interested in whether
the resulting number on the top face of the dice is a multiples of $3$.
We will first define the corresponding appropriate random variable $X$ such that
$X(\omega)=\text{'true'  for  } \omega \in ${$3,6$} and
$X(\omega)=\text{'false'}$ otherwise.
Then, the corresponding probability distribution is given by

$$P(X=b)
:=P(\omega\in\Omega | X(w)=b)=
\begin{cases}
  \displaystyle \frac{1}{3} \text{,   if   }b=\text{true}\\
  \displaystyle \frac{2}{3} \text{,   if   }b=\text{false}
\end{cases}$$

(For simplicity, we often denote $P(\omega\in\Omega | X(w)=b)$
$=P(X^{-1}(b))$
by its simpler expression $P(X=b)$, which is more common expression).
Thus, probability distribution is the functional description about the probabilities of
values of its associated random variable(s).

When the range of the random variable $X$ is countably-many,
$X$ is called <b>discrete (random) variable</b>
and its distribution is called <b>discrete probability distribution</b>.
When the range is uncountable,
$X$ is called <b>continuous (random) variable</b>
and its distribution is called <b>continuous probability distribution</b>.

When the range of $X$ is single-dimensional,
$X$ is called <b>univariate (random) variable</b>
and its distribution is called <b>univariate distribution</b>.
When the range is multi-dimensional,
$X$ is called <b>multivariate (random) variable</b>
and its distribution is called <b>multivariate distribution</b>.


<!---
probability mass function
cumulative distribution function
probability density function
population distribution
sample distribution
--->







