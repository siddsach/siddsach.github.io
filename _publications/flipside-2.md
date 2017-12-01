---
title: "FlipsideML"
excerpt: "Research Work for Flipside"

collection: portfolio
---

Code for my Flipside Research is in a Private Repo, but reach out if you're interested, I can share it in some cases

## Main Claim Detection Algorithm

I developed an algorithm that built on deep sentence representations, and combined extractive text summarization techniques with subjectivity analysis to identify the main opinions in a piece of persuasive writing. Traditional approaches that performed well in the literature of a Naive Bayes-Support Vector Machine only achieved 55% accuracy on this task, but my approach achieved 83% accuracy. In follow-up experiments examining the mistakes, I learned that this was because subjectivity in news and opinion requires more nuanced understanding to perform well at than mining subjectivity in product reviews where the literature evaluated in on. I combined a few pieces:

* MPQA Dataset
* [Deep Sentence Embeddings](https://arxiv.org/abs/1705.02364)
* [TextRank](https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf)
* Logistic regression

## Automatic Live Clustering 

![alt text](/images/bubbleviz.png)

We built an interactive visualizations of the different sides of an issue, based on people's votes on a particular claim. We combined a d3.js and vue.js front-end with regular HTTP requests to the backend to dynamically update this visualization as people voted. The methodology for the clustering went as follows:

* Constructs and Binary Agree/Disagree Votes Matrix
* Automatic Hyperparameter Tuning based on Sillhouette Score
* Perform Dimension Reduction (PCA, metric and non-metric MDS)
* Perform Clustering on new representations (KMeans, MeanShift)
* Construct Clustering Rationale using Statistical Feature Selection

## Devil's Advocate Recommendation System

I developed a system that used perspective topic models combined with a recommendation system to give people opposing points of view taylored to them. This system was able to generalize accurate predictions of recommendations to new articles based solely on text.

* Used [Perspective Topic Model](https://www.irit.fr/publis/SIG/2016_ECIR_TCBPS.pdf) to quantify different perspectives on various topics
* System able to unsupervisedly identify partisan slant for 87% of aricles
* Used in conjuction with my [recommendation system](https://github.com/siddsach/Hybrid-Recommender)
