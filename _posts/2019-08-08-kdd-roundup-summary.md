---
layout: post
title:  KDD Summary
tags:
  - data science
categories:
  - KDD 25 Roundup
---

Welcome to the final installment of my KDD 25 Roundup. Thursday was
the final day of the conference, so we had some concluding keynotes,
a little more time on the expo floor, and finally, tear down. I'm
taking this opportunity to reflect on the conference and summarize
lessons learned.

<!-- MORE -->

## Adversarial Defense

A series of talks at the [LEMINCS<i class="fa
fa-external-link"></i>][lemincs]{:target="_blank"} workshop
discussed and demonstrated weaknesses in the current generation of
deep learning and graph-based models to adversarial perturbations
(imperceptible, targeted adjustments to inputs which degrade
performance and change the model's predictions). These vulnerable
models span many domains, from cyber security to computer vision.

The state of the art has risen to address these vulnerabilities,
introducing a variety of defenses.

In the computer vision domain, we saw [SHIELD<i class="fa
fa-external-link"></i>][gh-shield]{:target="_blank"}, and [UnMask<i
class="fa fa-external-link"></i>][unmask]{:target="_blank"}. The
former introduces an ensemble of preprocessing defenses, while the
latter suggests an auxiliary model which verifies the output of the
main CV model. The interesting part about these contributions is how
they decouple defense from the model itself; they could give rise to
a generic defense framework that could be applied to a large
collection of models.

We've also seen a growing interest in the study of graph-based
models, particularly in cyber security. One of the LEMINCS keynotes,
*Adversarial Robustness of Machine Learning Models for Graphs*,
introduces a principled approach to injecting malicious,
imperceptible perturbations into data for a graph model, and that the
performance of many popular graph models can be degraded by this
method. The author went on to show how simple, non-graph models
outperform these attacked graph models, suggesting that if we can't
detect when a model has been attacked, it may be better to downgrade
to the baseline model.

[lemincs]: https://eda.cispa.saarland/events/lemincs19
[gh-shield]: https://github.com/nilakshdas/shield-efficacy
[unmask]: https://eda.cispa.saarland/events/lemincs19/papers/paper_freitas_etal.pdf

## Timeseries & Real-Time

Like graphs, timeseries analysis is a rapidly growing area of study,
with many potential uses in cyber. At KDD, we saw many innovations in
this space driven by engineering constraints and by borrowing
mathematics from other fields.

For example, we saw a real-time mobile diagnostics model required to
maintain nanosecond-order latency with 80+% accuracy, which
additionally learned dynamically from user feedback and 2-stage
classification. We also saw how Walmart executes anomaly detection at
scale as a means to locate and correct algorithmic pricing errors.

In [another example<i class="fa
fa-external-link"></i>][ms-ts]{:target="_blank"}, a presenter showed
how Spectral Residual Mapping and Convolutional Neural Networks
(borrowed form computer vision) can be used to detect anomalies
without a labeled dataset (and how to do so at scale with open source
tools).

[ms-ts]: https://arxiv.org/abs/1906.03821

## Attention

I, unfortunately, only saw one talk on the subject, but saw no fewer
than a dozen posters on it at one of the evening poster sessions.
Attention is a way for neural networks to prioritize different
features *during inference* based on the values of the input vector.

It seems to be a promising way to make models more aware of and
adaptive to context, and indeed, *Real-Time Attention-Based
Look-Alike Model for Recommender Systems* (or [RALM<i class="fa
fa-external-link"></i>][ralm]{:target="_blank"}) backs this up. The
authors presented a neural network architecture which leveraged
attention mechanics to incorporate user context more strongly into a
recommender system, with striking results.

This approach seems promising in more domains than recommendation, so
I'm excited to dig deeper!

[ralm]: https://arxiv.org/abs/1906.05022
