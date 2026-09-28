# Summary of fundamentals concepts in Machine Learning
## Purpose: inferring general functions from known data
The ML studies and proposes methods to build (**infer**) functions (also called as **hypothesis**) from examples of observed data (world observations), such that:
- fit the known examples
- are able to generalize, with reasonable accuracy for new, unseen data (see later for the specific criteria)
- the learning process is subject to *biases* ("inductive bias", see later)
## The main ingredients
- Data
- Task
- Model
- Learning Algorithm
![ingr](Ingredients1.jpg)
## Types of tasks
- **predictive** (such as classification/regression): the goal is to find an *approximation* of the model/function
- **descriptive** (such as cluster analysis/ Association Rules): find subsets or groups in unclassified data

## Supervised Learning
We give to the *learner* model a training set (TR) made of examples in the form of **labeled** data ( $ \rightarrow$ a set of pairs $<x, d>$ where d is the output (**target value**) of the unknown function $f(x)$ (**target function**) that we want to infer).
The learner has then have to find a "*good*" (kind of sloppy, this will be clarified later) approximation of $f(x)$, that can be used to predict outputs of unseen data, $x'$. 

Examples of supervised learning:
- regression (inferring a real-valued function)
- classification (inferring a discrete-valued function)

### Regression
![lin_regr](Regression1.jpg)

## Unsupervised Learning
This time there's no teacher that shows to the learner the target values of the inputs: the training set is made of **unlabeled** data ($<x>$). A common task is to find natural groupings in a set of data (e.g: clustering, dimensionality reduction, modeling data density)

## Definitions
- **Hypothesis** = a proposed function $h$ believed to be similar to $f$. Its representation depends on the "language" (numerical, symbolic) that describes the relationships among data.
- **Hypothesis space (H)**: The space of all hypotheses (specific models) that
can, in principle, be output by the learning algorithm.
- **Learning algorithm**: it's a search through the hypothesis space H of the best hypothesis.
Typically the learning is based on a local search approach:
![loc_search](local_search1.jpg)

## Inductive Bias
![ind_bias](Inductive_bias1.jpg)
## Finding the Version Space
- "consistency": a hypothesis $h$ is said consistent with the TR, if $h(\mathbf{x}) = d(\mathbf{x})$ for each training example $<\mathbf{x}, d(\mathbf{x}) >$ in TR.
- **Version Space** (VS): is the subset of hypotheses from H consistent with all training examples.
