

Applied Modeling Talk
========================================================
author: Jared Knowles
date: October, 2013

Do machines really learn?
========================================================

Applied modeling goes by many names: statistical learning, machine learning, and 
data mining. 

The key differences between applied modeling and statistical inference are:

- Emphasis on predictive validity
- De-emphasis on parameter values
- Test and training data
- Measures of fit


Goals for This Talk
========================================================

1. Introduce the world of statistical models outside of 
linear models
2. Demonstrate the specific techniques around building predictive models
3. Discuss the tradeoffs in applied vs. research models
4. Show some R code!


Applied Models and Inference
========================================================

Applied modeling and inferential statistics share many of the same concepts:

- Regression estimation
- Concerns about representative of data and samples
- Fear of outliers
- Robustness and sensitivity

<img src="AppliedModelingTalk-figure/unnamed-chunk-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />



Why the Difference?
========================================================

Applied Models:

- Provide information to users about what to expect given certain data
- Goals for the model are defined by the needs of the users

***

Inferential Models: 

- Seek to learn about the relationships in the data at hand
- Focused on understanding patterns in the current data


Some Vocabulary
========================================================

- Training data
- Test data


***

- Data the model is fit to
- Data the model is applied to, but not fit to, to evaluate model fit

