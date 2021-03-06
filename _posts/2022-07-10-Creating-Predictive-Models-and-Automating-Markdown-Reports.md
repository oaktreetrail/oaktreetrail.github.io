ST558 Project 2: Creating Predictive Models and Automating Markdown
Reports
================
Lan Lin
2022-07-10

## Brief Description of Repo

This report will be analyzing and fitting models on the Online News
Popularity Data Set from UC Irvine’s machine learning repository. This
data looks at nearly 60 variables and tries to predict the number of
shares that an article will get. We will be performing some basic
exploratory data analysis with tables and graphs, then will fit some
models on the data to try to predict the number of shares an article
gets. We subset the number of predictors to about 30. Many of the
predictors in the data set are indicator variables, which indicate
things like day of the week or data channel. Other important predictors
include article word count, number of videos or images or links in the
article, the rate of positive or negative words, and more. When fitting
the models, we split the data 70/30 into training and testing sets,
respectively. We will be fitting four models on the training data: two
linear regression models, a random forest model, and a boosted tree
model. At the end, we will be comparing the root mean square error
(RMSE) of each model on the testing set and decide which one performed
the best.

## Things I would do differently next time

This project mainly focused on how to automate Markdown Reports. So, we
did not spend two much time on transforming and tunning the predictive
models and the adjust R square values are pretty low. I would make our
models having more predictive power for the response next time.

## The most difficult part for me

I had a brief idea on how to automate Markdown Reports, and I understood
we needed to specify the channel file names in the YAML header. But I
don’t know how to push the automation documents up to GitHub. I found
this part most difficult.

## The big take-aways from this project.

Parameterized reports allow us to specify one or more parameters to
customize the analysis. This is useful if we want to create a report
template that can be reused across multiple similar scenarios.

## Below are the links to our project

\-[GitHub page repo is available
here](https://github.com/oaktreetrail/ST558_Project2)

\-[Regular repo is available
here](https://oaktreetrail.github.io/ST558_Project2/)
