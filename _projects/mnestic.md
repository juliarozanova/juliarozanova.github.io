---
title: Mnestic Probing
layout: page
permalink: /mnestic/
usemathjax: true
---

A short, friendly summary of my favourite contribution from my PhD work. With pictures!

## Introduction
<!-- Our probing study showed that after fine-tuning on HELP, models showed an increased distinction between
upward and downward monotone contexts, which they strongly lacked beforehand. -->

<!-- 
This gave us a better indication that the models have actually "learned" the concept of monotonicity,
in a more qualitative way than just "more training on more data = greater accuracy". -->

A core theme of my PhD work was the **interpretability** of language models: 
in particular, which linguistic features that the model is *not* explicitly trained to detect still 
emerge as linearly separable clusters within the vector representations of text? 
Methodology such as **probing** is sometimes used to argue that a given **auxiliary feature** is 
detectable in a model's representations.

A common criticism of probing (and there are many) is that even if an auxiliary feature is
linearly separable in the representations, this does not imply that this feature is used for the model's
final prediction. 
One of the papers I obsessed over the most during my PhD was [Amnesic Probing: Behavioral Explanation with Amnesic Counterfactuals](https://arxiv.org/pdf/2006.00995.pdf) by Shauli Ravfogel and Yanai Elazar, which attempts to address this limitation with a new methodology.

It starts by assuming we have the following setup: 
Suppose we have a neural model $f$ trained on a dataset $(X, Y)$, where each $x_i \in X$ is a textual input and $y_i \in Y$ is the corresponding **task label** (the task label
corresponds to a high-level objective such as language modelling or natural language inference).
We may treat $f$ as a composition of two functions: an encoder $h$ and a classifier $c$, such that $f(x) = c(h(x))$.

<img src='/assets/Website_Mnestic.svg' width="600">

Suppose it is already known that we may train an auxiliary linear classifier $g$ on the set of encoded vector 
representations $H = h(X)$ for a set $Z$ of **auxiliary labels** and achieve a high accuracy. 
These auxiliary labels $Z$ could be something like part-of-speech tags, gender labels, or lexical relations: any information about the base text input $x$ that the model $f$ is not already trained to classify.

<img src='/assets/Website_Mnestic _Probe.svg' width="500">

The amnesic probing paper asks if it is possible to *remove* the part of the encoded representations $H$ that is informative about the labels $Z$.

Can we define a vector transformation $d$ such that $d(h(X))$ is a **debiased** representation of the dataset $X$, in the sense that 
- we can no longer learn to predict $Z$ from $d(h(X))$ with any new linear probe
- $d(h(X))$ is in the same representation space as $h(X)$, and can serve as an input to the task classifier $c$


## The Amnesic Intervention: Iterative Nullspace Projection



## The Mnestic Intervention: Don't Forget, Remember!

Much to my dismay, it translated poorly to my problem space - the amnesic interventions had almost no impact on the RoBERTa representations, even for features for which it absolutely should have.








## An Amesic Intervention: Iterative Nullspace Projection

There are some good discussions of its limitatons: 
[[probing ineffective]] discusses how certain colinearity properties ensure that amnesic probing will not remove target features.




