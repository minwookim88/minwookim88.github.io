---
layout: posts
title:  "Tips in Data Analysis"
date:   2019-03-08 20:00:00 -0700
categories:
  - data_science
  - Tips
tags:
  - tips
---

Here are some tips that I learned from analyzing actual, real-world data.
<ol>
  <li>Don't jump into model first. Spend enough time in understanding data first.</li>
  <li>At the beginning, study the domain where the data came from. Spend as much time in studying the domain as you would spend with the data itself. Studying the domain is important because it helps in understanding
<a href="{% link _posts/2019-05-07-Data Encodes Information.md %}">missing piece of the data</a></li>.
  <li>In preliminary analysis, try to visualize data to better understand data.</li>
  <li>Try to understand general trend in data before applying complex model. To do so, pick some of the instances of sample and dig into those examples (case-study).</li>
  <li>When doing case-study, start with the most anomlous data. Those are the easiest example candidates to understand strong causational relationship.</li>
  <li>Always start with the simplest model. Gradually upgrade your model as you gain more and more insight from simpler models.</li>
  <li>Start with unsupervised learning method first. Even if you have label data, don't trust it first. This is essentially an extension of case-study, by grouping similar data together to see general pattern within them <i>per group</i>.</li>
  <li>Do not always try to build one grand, global model. Break data into subgroups where they show similar patterns within group, and build respective models for each group.</li>
</ol>