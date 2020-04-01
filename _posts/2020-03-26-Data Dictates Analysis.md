---
layout: posts
title:  "Data Dictates Analysis"
date:   2020-03-26 20:00:00 -0700
categories: data_science topsy-turvy
---
When we do data analysis, we often neglect that the fact that data is the biggest and the most important part of the whole analysis process. Depending on the information it contains, it dictates overall direction of the upcoming analysis - it helps us to define specific problems to solve from rather raw, project-oriented broader objectives; then it further determines which methodologies and algorithms need to be used in order to achieve the goals. Thus, data is more than just a gimmick for an analysis project. If there is a huge discrepancy between the goal of a project and the actual information available in the data, we need to either step back and redirect the project or try to get new data that looks more promising.

<figure>
  <img src="/assets/images/analysis_flow.png">
  <figcaption>Analysis Flow</figcaption>
</figure>

However, we often see a lot that people suddenly jump into talking about models even before they fully dig into data. Also, if you are a data scientist or analyst, you might have heard a lot that people ask you, "What kind of models do you use in your analysis?". To me, it sounds like "What kind of formulas or theories do you use when solving math problem?". It is kind of okay if the conversation is informal and thus is just for social purposes, but otherwise I seriously recommend to give it a second thought in wasting your precious time with him/her.

<figure>
  <img src="/assets/images/data_model.png">
  <figcaption>Data vs Model</figcaption>
</figure>

Data should be the main player on the field that dictates analysis plan. You cannot learn insights from data without digging into data. Without insights, you cannot define proper, solvable problems because you don't even know whether the answer you are looking for even exists in the data. Without proper problem statement, you cannot choose right models. It doesn't make sense you talk about CNN (Convolutional Neural Network) just because you got image data in your hand. What if there is no label at all? What if there is label but the information is very subjective and thus is not reliable? What if there are not sufficient number of samples to ensure enough variance within the samples?

Data analysis is the process of analyzing the given data. It's not like analyzing data given a model. Only after you understand what type of information exists in data can you choose a model that is designed to extract that particular information. This means you need to thoroughly study the data through EDA (Exploratory Data Analysis) before running any algorithm, so that you can catch the nuance and the insights behind it.

<figure>
  <img src="/assets/images/eda.png">
  <figcaption>Example of EDA Plots</figcaption>
</figure>

EDA allows you to develop a good sense of intuition into data on your own through observation and case-study. Then, based on this preliminary analysis, you can set up hypotheses that you might want to test. Choosing and running a model is just a supplementary step for validating your initial observations in a quantitive manner on a bigger scale, so that you can rightfully justify your claim by generalizing initial observation quantitatively. Model training can never replace EDA's role of insight extraction, so it should never precede and substitute EDA step. The result from model without a priori EDA step is nothing but one out of millions of arbitrary stories you can fabricate from data. Digging into data allows you to have an insight into picking and choosing most realistic stories out of them.

As we have seen so far, data is the main ingredient in data analysis. So, it should be really helpful in doing data analysis if we can deeply understand the nature of data itself. We will dig into it more in detail in the next several subsequent posts.