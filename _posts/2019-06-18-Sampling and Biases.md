---
layout: posts
title:  "Data Acquisition and Sampling"
date:   2019-06-18 20:00:00 -0700
categories:
  - data_science
  - topsy-turvy
tags:
  - sampling
  - sample
  - population
  - bias
  - variance
  - tradeoff
---
Suppose one day we happen to observe a phenomenon that occurs in nature.
If it is the first time, it won't be easy to informationalize the observation
(i.e. [transform the observation into information]({% post_url 2019-04-03-Information Abstracts Truth %})),
because we are not sure which part of the phenomenon is repetitive and which part is not.
If the whole phenomenon itself is completely unique that is not of repetitive nature,
any information made out of the observation is no useful in that
it is not reusable - we know that the time will never come
when we will be able to take advantage of the information because the underlying phenomenon was unique and will never occur again.

So, for the observation and information to be useful, the underlying phenomenon needs to be repetitive and re-occuring to a certain extent.
In order to check whether the underlying phenomenon is completely out of coincidence (and thus unique) or repetitive in some sense so that the information is generalizable (and thus reusable), we need to be able to observe as many similar happenings as possible.

However, as we briefly mentioned in [this post]({% post_url 2019-04-03-Information Abstracts Truth %}),
we are not allowed to observe everything in the world
due to inherent limitations by time and space.
As a consequence, we are forced to choose only a limited number of candidates for observation that we can use in justifying and generalizing our findings - which is called <b>sampling</b>.

<b>Sampling</b> refers to the process of selecting <u>a list of candidates</u> (called <b>sample</b>) for observation out of <u>all observable objects in the universe</u> (called <b>population</b>). It is a technique that is used to walk around the need to observe everything, while ensuring that these candidates are sufficiently representative of the entire universe in the sense that the findings from the candidates are close to those from the universe.

So, the purpose of sampling is to find (1) <u>good enough samples to well-represent the population</u>,
while (2) securing <u>enough number of samples to be able to generalize findings</u> out of them, at the same time (3) <u>alleviating the burden of observing too many samples</u>.




Issue related with (1) is <b>bias</b> problem,
and the issue between conflicting (2) and (3) is <b>cost-reliability tradeoff</b>.


<b>bias-variance tradeoff</b>.



These two criteria are conflicting sometimes, because if we select too few number of samples,
there is low change of finding 


they need to be generalizable to a certain extent. 

as we observe more, we can generalize
