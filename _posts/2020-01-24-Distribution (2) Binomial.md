---
layout: posts
title:  "Distribution(2): Binomial"
date:   2020-01-24 20:00:00 -0700
categories:
  - Math
  - Probability_Theory
  - Stat
  - data_science
---
<b>Binomial distribution</b> is a
[probability distribution]({% post_url 2019-09-14-Random Variable and Distribution %})
where the associated random variable $X$ takes only two values - $0$ and $1$;
that is, the range of the random variable function
$X:\Omega \rightarrow ${$0,1$} that encodes outcomes of sample space
is binary.
The distribution is usually denoted by $\mathcal{B}(p)$, where
$p$ is the parameter that encodes
the probability $p:=P(X=1)$.

In Statistics, the distribution is used to model a system where
a researcher is only interested in two disjoint events
$A:=${$X=0$}$={X^{-1}(0)}$ and
$B:=${$X=1$}$={X^{-1}(1)}$
from observation of the system.
For example, suppose a researcher is interested in
knowing the number of people whose height is
greater than $2$m(=$200$cm) in California.
As he measures a
[sample]({% post_url 2019-06-18-Sampling and Biases %})
of people,
all he needs to know is whether the person is taller than $2$m or not;
not the exact height.
So, instead of encoding $X_i=185$(cm)
for $i^{\text{th}}$ sample, he might as well just encode as
$X_i=$true or false - binary.

Bernoulli distribution is the most simplest form of distribution of all distributions, yet it is the root distribution that provides
theoretical foundations of other important distributions, including but not limited to
<b>binomial</b>, <b>categorical</b>, <b>uniform</b>, <b>geometric</b>, <b>normal</b>, <b>exponential</b> and <b>poisson distribution</b>.
<!---
https://en.wikipedia.org/wiki/Probability_distribution
--->