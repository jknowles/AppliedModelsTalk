<style>

body, p, td, li, div {
  font-size: 18pt;
  color: white;
}

h1,h2,h3,h4,h5,h6 {
	text-shadow: 0 0 0 #000 !important;
  color: white;
}


.reveal .state-background {
  background: black;
} 

.reveal section p {
  color: white;
}

.reveal section h1 {
  color: white;
}

.reveal section h2 {
  color: white;
}

.reveal section h3 {
  color: white;
}

</style>

Using Statistical Models to Help Policymakers Avoid Mistakes
========================================================
author: Jared Knowles
date: October 23, 2013

Overview
===============

- What mistakes do policymakers make?
- What tools can be used to avoid them?
- How do you make the case to avoid these mistakes?
- Your toolkit needs to be broad to meet policymakers needs

Mistakes We Knew We Were Making
======================================

Three vignettes will serve to ground our discussion on common mistakes in 
the policy world using data. No policymaker is immune to making any of these 
mistakes and even trained analysts can, do, and will make them.

1. The case of the simple mean
2. Why rates are always leading us astray?
3. Applying models improperly


Problems with the mean
========================

1. The mean is uninformative because it masks conditional variation
2. The mean invites overinterpretation too often
3. The mean too often substitutes important facts about the rest of the distribution

Expecting and presenting only the mean masks too much heterogeneity and too much 
important variability to invite systemic or productive analysis. 

The Mean is Uninformative
============================

Gap

- Black-white gap is 1 standard deviation
- Economic disadvantage gap is 1 standard deviation
- SwD gap is 1.2 standard deviations

***

Alternative hypothesis

- Black students are more likely to be poor
- Poor students are more likely to be black
- Disabled students are more likely to be black or poor

The Mean is Misinterpreted
=============================

Gap

- Black-white gap is 1 standard deviation
- Economic disadvantage gap is 1 standard deviation
- SwD gap is 1.2 standard deviations

***

Alternative: 

- All black students underperform white students
- Economically disadvantaged students do not score highly on tests
- Having any disability drastically reduces your student performance


The Mean Masks too Much
===================================

Gap

- Black-white gap is 1 standard deviation
- Economic disadvantage gap is 1 standard deviation
- SwD gap is 1.2 standard deviations

***

Hidden facts: 

- In some schools a white-black gap exists
- Some economically disadvantaged students are indistinguishable from their peers
- Some disability types outperform students without disabilities

The Kicker
===========================

Students who are black, economically disadvantaged, and disabled have much worse 
student outcomes than would ever be considered from the statistics above. 

Students who are white, economically disadvantaged, and disabled have much better 
outcomes than their black peers. 

These facts cannot be uncovered by simple means. 

An Aside on Skew
=============================

<img src="AppliedModelingTalk-figure/graph1.png" title="plot of chunk graph1" alt="plot of chunk graph1" style="display: block; margin: auto;" />



Tools to Address the Mean Problem
===========================================

- Data visualizations
- Conditional probability models
- Discussions

<img src="AppliedModelingTalk-figure/graph2.png" title="plot of chunk graph2" alt="plot of chunk graph2" style="display: block; margin: auto;" />


Plot The Effects
=========================
<img src="AppliedModelingTalk-figure/effplot1.png" title="plot of chunk effplot1" alt="plot of chunk effplot1" style="display: block; margin: auto;" />


Plot The Effects: Categorical
==============================
<img src="AppliedModelingTalk-figure/effplot2.png" title="plot of chunk effplot2" alt="plot of chunk effplot2" style="display: block; margin: auto;" />


Problems with the rate
========================

1. The rate is not robust in small groups
2. The rate masks uncertainty
3. The rate does not provide a proper sense of inertia

Rates are often turned to when wishing to explain the differences between areas 
with different group sizes. This can be misused and cause bad policy responses. 


Graduation rates
=========================

Exercise: Describe a school district with the lowest graduation rate in 
your favorite state. 


Graduation rates
=========================

What features did you use to describe it? 

1. High poverty
2. High minority
3. Large urban core?

In Wisconsin the lowest graduation rate in the state belongs to a district with 
under 250 students in a graduating class. 

Only **103** out of **228** students in Grantsburg graduated in 2011-12. 

Two Comments and a Question
===============================

1. If Grantsburg graduated 50 more students in a year, it would move past several 
other districts in the state. 

2. If MPS graduated 500 less students in a year, it still would not fall below 
Grantsburg. 

Is it fair to rank Grantsburg below Milwaukee? It probably depends!

Fragility of Rates
======================

Consider Prentice. 

<img src="AppliedModelingTalk-figure/pregraph.png" title="plot of chunk pregraph" alt="plot of chunk pregraph" style="display: block; margin: auto;" />


The Problem
====================

1. Is Prentice above or below average?
2. What will Prentice's rate be next year?
3. How easy is it to move the rate?

And all of these problems are if we ignore the problems about unconditional 
probabilities we have already discussed!

Applicability
==========================

This is why ranking systems are suspect rating period to rating period. Simply 
reporting the rate provides no underlying sense of the variability in the measure and 
without also reporting the *n* count, there is no way to interpret the findings. 

If you work in policy you will be asked to report means and rates all the time. 

You will be asked to construct rankings and indexes all the time. 

Tread carefully!

Solutions
=============

1. Present rates with robustness by simulating change in rate with change in 
unit level 
2. Conduct ecological inference on group data to infer probabilities for 
individual units with uncertainty
3. Use Bayesian methods to pool across groups and appropriately estimate uncertainty for small groups, and certainty for large groups

Solutions - Quick and Easy
==============================

For repeated measures we can report the rate with "fragility" by showing the 
range if 3 or 4 more students graduated or did not graduate.

<img src="AppliedModelingTalk-figure/pregraph2.png" title="plot of chunk pregraph2" alt="plot of chunk pregraph2" style="display: block; margin: auto;" />








Solutions - Interesting
=============================

Without individual level data, we can use something called *ecological 
inference* to try to understand the probability of individual behavior. 


```r
print(head(senc[, 2:9]))
```

```
       precinct total white black natam  dem rep non
1       ABBOTTS   490   355   134     1  399  61  30
2        BETHEL  1729  1497   224     8 1238 343 148
3   BROWN MARSH  1363   817   541     5 1132 150  81
4 CARVERS CREEK  1172   202   889    81 1032  60  80
5       CENTRAL   470   298   170     2  379  40  51
6         COLLY   974   784   183     7  674 205  95
```


Solutions - Ecological Inference
=================================


























```
Error in prettyNum(.Internal(format(x, trim, digits, nsmall, width, 3L,  : 
  invalid 'digits' argument
```
