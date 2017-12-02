---
title: "Flipside Research"

collection: portfolio
---

Code for my Flipside Research is in a Private Repo, but reach out if you're interested, I can share it in some cases

## Main Claim Detection Algorithm

I developed an algorithm that built on [deep sentence representations](https://arxiv.org/abs/1705.02364), and combined [extractive text summarization techniques](https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf) with supervised [subjectivity classification](http://mpqa.cs.pitt.edu/corpora/mpqa_corpus/) to identify the main opinions in a piece of persuasive writing. Traditional approaches that performed well in the literature of a Naive Bayes-Support Vector Machine only achieved 55% accuracy on this task, but my approach achieved 83% accuracy. In follow-up experiments examining the mistakes, I learned that this was because subjectivity in news and opinion requires more nuanced understanding than in product reviews where the literature evaluated on to perform well.


## Automatic Live Clustering 

![alt text](/images/bubbleviz.png)

Motivated by research on [casual information visualization](https://dl.acm.org/citation.cfm?id=1313)We built an interactive visualization of the different sides of an issue, based on people's votes on a particular claim. We combined a d3.js and vue.js front-end with regular HTTP requests to the backend to dynamically update this visualization as people voted. The methodology for the clustering went as follows:

* Construct Binary Agree/Disagree Votes Matrix
* Perform Dimension Reduction (PCA, metric and non-metric MDS)
* Perform Clustering on new representations (KMeans, MeanShift)
* Automatic tune Hyperparameters based on Sillhouette Score
* Construct Clustering Rationale using Statistical Feature Selection

## Devil's Advocate Recommendation System

Motivated by [political psychology research on the effects of language](http://journals.sagepub.com/doi/abs/10.1177/0146167215607842), I developed a system that used perspective topic models combined with a recommendation system to recommend people opposing points of view tailored to them. This system was able to generalize accurate predictions of recommendations to new articles based solely on text.

* Used [Perspective Topic Model](https://www.irit.fr/publis/SIG/2016_ECIR_TCBPS.pdf) to quantify different perspectives on various topics
* System able to unsupervisedly identify partisan slant for 87% of aricles
* Used in conjuction with my [recommendation system](https://github.com/siddsach/Hybrid-Recommender)
