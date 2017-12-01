---
title: "FlipsideML"
excerpt: "Research Work for Flipside"

collection: portfolio
---

Code for my Flipside Research is in a Private Repo, but reach out if you're interested, I can share it in some cases

## Main Claim Detection Algorithm combining a few things

* MPQA Dataset
* [Deep Sentence Embeddings](https://arxiv.org/abs/1705.02364)
* [TextRank](https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf)
* Logistic regression

## Automatic Live Clustering 

![alt text](/images/bubbleviz.png)
Built Automatic Clustering Class that 

* Constructs and Binary Agree/Disagree Votes Matrix
* Automatic Hyperparameter Tuning based on Sillhouette Score
* Dimension Reduction (PCA, metric and non-metric MDS)
* Clustering (KMeans, MeanShift)
* Constructs Clustering Rationale using Statistical Feature Selection

## Devil's Advocate Recommendation System

* Used [Perspective Topic Model](https://www.irit.fr/publis/SIG/2016_ECIR_TCBPS.pdf) to quantify different perspectives on various topics
* System able to unsupervisedly identify partisan slant for 87% of aricles
* Used in conjuction with my [recommendation system](https://github.com/siddsach/Hybrid-Recommender)
