<style>

body, p, td, li, div {
  font-size: 18pt;
  color: white;
}

h1,h2,h3,h4,h5,h6 {
        text-shadow: 0 0 0 #000 !important;
  color: white;
}

.section .reveal .state-background {
   background: black;
}

.section .reveal h2,
.section .reveal h3,
.section .reveal p {
   color: white;
   margin-top: 50px;
}


.reveal blockquote {
  background: black;
  border-left: 10px solid #ccc;
  margin: 1.5em 10px;
  padding: 0.5em 10px;
  quotes: "\201C""\201D""\2018""\2019";
}

.reveal section del {
  color: red;
}

blockquote:before {
  color: #ccc;
  content: open-quote;
  font-size: 4em;
  line-height: 0.1em;
  margin-right: 0.25em;
  vertical-align: -0.4em;
}

blockquote p {
  display inline;
}

.reveal pre {   
  margin-top: 0;
  max-width: 95%;
  border: 1px solid #ccc;
  white-space: pre-wrap;
  margin-bottom: 1em; 
  color: black;
}

.reveal a:not(.image) {
  color: red;
  text-decoration: none;
  -webkit-transition: color .15s ease;
  -moz-transition: color .15s ease;
  -ms-transition: color .15s ease;
  -o-transition: color .15s ease;
  transition: color .15s ease; }

.reveal a:not(.image):hover {
  color: #0000f1;
  text-shadow: none;
  border: none; }

.reveal .roll span:after {
  color: #fff;
  background: #00003f; }

.reveal pre code {
  display: block; padding: 0.5em;
  font-size: 1.6em;
  line-height: 1.1em;
  background-color: white;
  overflow: visible;
  max-height: none;
  word-wrap: normal;
  color: black;
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

<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    "HTML-CSS": { scale: 100}
  });
</script>

Statistical Learning and Applied Modeling in Education
========================================================
Examples and Concerns
------------------------------------------------------

## **Jared Knowles**
## **01-31-2014**

Motivation
===================================================
incremental: true

- What does it mean to be data driven?
- What can we learn from NLSY, ELS, ECLS?
- What can we learn from administrative records?
- How can we provide educators and decision makers with a sense of what **might** happen, 
instead of what **may have** happened?

Some Trends
======================================================

- Available data in education is growing astronomically. 
- Schools are increasingly being asked to provide more services. 
- Policy makers increasingly asked to justify their policies with projections. 
- Timelines are speeding up!

Outline
=====================================================

- Statistical Learning
- Preparing Data
- Assessing Model Fit
- Applying Models Beyond the Journal Article


What is a statistical model?
===============================

- "All models are wrong, some models are useful"
- Being wrong is a **feature of a statistical model**, the goal is to explain 
as much data as possible with as few variables as possible
- Statistical models are mathematical summaries of correlations and probabilities 
of known data
- The most common form is the linear regression model

Statistical Modeling
=======================================================

It is useful to remember that in statistical modeling, in the **supervised** case, we are looking at the following relationship:

$$ \hat{Y} = \hat{f}(X) $$

In this case $\hat{f}$ represents our estimate of the function that links $X$ and 
$Y$. In traditional linear modeling, $\hat{f}$ takes the form:

$$ \hat{Y} = \alpha + \beta(X) + \epsilon $$

However, there exist limitless alternative $\hat{f}$ which we can explore. Applied modeling techniques help us expand the $\hat{f}$ space we search within.

Functional forms
==============================

<img src="AppliedModelinginEducation-figure/unnamed-chunk-1.png" title="Figure Adapted from James et al. 2013" alt="Figure Adapted from James et al. 2013" style="display: block; margin: auto;" />


Figure adapted from James et al. 2013 (figure 2.7)

Why the Difference?
========================================================

Applied Models:

- Provide information to users about what to expect given certain data
- Serve many goals including prediction of non-observed 
outcomes, summarizing large datasets, measuring uncertainty
- Goals for the model are defined by explicit tradeoffs

***

Inferential Models: 

- Focused on understanding patterns in the current data
- Seek to understand how current data extrapolates to a population
- Estimates population parameters from sample data to inform on relationships


Some Vocabulary
========================================================

- Training data
- Test data
- Bias (error)
- Variance (error)


***

- Data the model is fit to
- Data the model is applied to, but not fit to, to evaluate model fit
- Refers to the amount of error due to simplifying a complex process
- The amount the $f$ would change if fit to a different training set of data


The Challenge
=================================

- When using a statistical model to make predictions we have to think clearly 
about the data we use to build the model, and the data we will be making 
predictions about
- We may build a model with high **internal validity** for the data at hand, 
but that data may not be representative of the data the model will apply to
- We call this the **training error** and the **test error**
- In inferential statistics we often seek to reduce **training error** and not 
concern ourselves with **test error**
- In applied modeling we focus on finding the optimal tradeoff between **variance error** and **bias error** 

Preparing Data
=================================================

1. Recoding variables
2. Centering and scaling


Evaluating Model Fit
==================================================

1. Training and test fit
2. Classification measures
3. Cross-validation
4. Setting thresholds


Model Fit
==================================================

<img src="AppliedModelinginEducation-figure/unnamed-chunk-2.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />


Adapted from Bowers and Sprott 2013

What Changes When a Model is Actually Used?
==================================================

Missing Data Issues
==================================================



Further Resources
====================

- The Signal and the Noise: Why So Many Predictions Fail  but Some Don't. Nate Silver. (2012). Penguin.
- The Black Swan: Second Edition: The Impact of the Highly Improbable (2nd ed. 2010). Nassim Taleb.  Random House.
- An Introduction to Statistical Learning (2013). Gareth James, Daniela Witten, Trevor Hastie and Robert Tibshirani. Springer. 
- Elements of Statistical Learning (Second Edition, 2011). Trevor Hastie, 
Robert Tibshirani, and Jerome Friedman. Springer