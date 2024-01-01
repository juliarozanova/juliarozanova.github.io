---
title: Probe-Ably
layout: page
permalink: /probeably/
---

## Introduction

Blackbox neural models such as LLMs are notoriously opaque. 
In the interest of model interpretability, researchers may want to examine the properties of their models' representations.

*Probing* is the use of external/secondary models to determine how easily an auxiliary feature which a model was *not* explicitly 
trained to detect can be learnt from its intermediate vector representations. 

However, probing results in isolation can be misleading: we designed Probe-Ably to promote the practice of training *multiple probes* 
with varying complexities and to compare curves rather than interpreting isolated probing accuracy values.

Check out the [docs](https://ai-systems.github.io/Probe-Ably/), [github page](https://github.com/ai-systems/Probe-Ably) and [ACL systems demo paper](https://aclanthology.org/2021.acl-demo.23/) for full details!

## Initial Steps

While I was getting started on applying probing methods in the first major paper of my PhD, [Decomposing Natural Language Inferences in Neural NLi](https://aclanthology.org/2022.blackboxnlp-1.33/), a few of my PhD lab mates showed interest in using probing techniques in some of their own projects. We quickly saw the value in developing 
a shared framework. 

To get them on board, I started off by presenting a playfully informal slide deck which summed up my recent reading, giving an overview
of the probing research landscape (representative of late 2020), which was evolving rapidly at the time. We were especially keen to incorporate 
new metrics and principles adressing known limitations of probing techniques.
<iframe src="https://slides.com/juliarozanova/probing-landscape/embed" width="576" height="420" title="Probing Landscape" scrolling="no" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

After this, Probe-Ably happened very quickly: we soon realised that we were conveniently close to the ACL systems 
demonstration paper submission date, and this motivated us to do a hearty push on the project. 
Between the four of us, we had a working prototype within a matter of days, and a paper within the following week. 
Much to our delight, it was accepted!

## Team

<img src='/assets/IMG-20221208-WA0010.jpg' width='600'>

From left to right:
Mokanarangan Thayaparan, Marco Valentino, Julia Rozanova, Deborah Ferreira

## Limitations? Next Steps?
Because the research on model interpretability is expanding so fast, Probe-Ably has very much become
specific to its time - while the base principle of training and comparing multiple probes across various 
complexities remains useful, there are many evolving techniques and best practices that are beyond Probe-Ably's 
current scope.
We don't have plans to extend Probe-Ably ourselves - further work in this direction is more likely to be a whole new thing!