+++
date = "2018-01-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "probabilistic_timeseries_modelling"
short_description = "Probabilistic Time Series Modelling"
title = "Probabilistic Time Series Modelling"
[[participants]]
    name = "Ingmar Schuster"
    is_member = true
    id = "ingmar_s"
[[participants]]
    name = "Kashif Rasul"
    is_member = true
    id = "kashif_r"
[[participants]]
    name = "Urs Bergmann"
    is_member = true
    id = "Urs_b"
[[participants]]
    name = "Calvin Seward"
    is_member = true
    id = "calvin_s"
[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"

+++

## Research Project by [Ingmar Schuster](/member/ingmar_s), [Kashif Rasul](/member/kashif_r), Urs Bergmann, [Calvin Seward](/member/calvin_s), & [Roland Vollgraf](/member/roland_v)

This project aims at probabilistic time series models, which is a general problem setting across many modern internet companies. In other words, we want to be capable of getting a predictive distribution for the value of a time series at future time points from our model. Such solutions are widely applicable to a number of Zalando use cases for example demand and trend forecasting or detecting anomalous behaviour. Probabilistic models also help our stakeholders to better assess the risk associated with any forecast and provide a way to quantify the uncertainty associated especially when predicting far into the future. We currently follow two main approaches, one based on a recurrent neural network, the other on reproducing kernel hilbert space (RKHS) operators.

In the deep learning approach, a long short-term memory (LSTM) architecture is trained to, given past measurements, output parameters for a family of distributions such that observed data at the current time has a high likelihood [2,3]. For future time points, several samples from the predictive distribution are used in order to propagate uncertainty. We use embeddings [1] to encode categorical covariates and develop techniques to model interactions or correlations between different time series.

![image1](img/image15.png) ![image2](img/image23.png)

The RKHS based approach on the other hand uses recently developed RKHS operator ideas in order to get an estimate of the distribution for the current time, given past measurements. Different from a classical regression task we seek to provide a full estimate over the distribution of the output variable given the input. Nonparametric closed form solutions exist for the operator of interest, which however do not allow to place certain constraints on the obtained solutions. For this reason and to keep model complexity under control, we employ stochastic gradient optimization algorithms. The resulting method captures uncertainty like Gaussian Processes, but unlike these is neither bound to Gaussian distributions for the output nor to real domains or univariate outputs.

Also, it is not bound to describe time series models, but can be used for any distribution regression task.

![image3](img/image3.png)

References

<span class="c5">[1]</span> <span class="c5">Guo, C. &</span><span class="c5"> </span><span class="c5">Berkhahn, F. (2016).</span> <span class="c5">Entity Embeddings of Categorical Variables</span> <span class="c6">[https://arxiv.org/abs/1604.06737](https://www.google.com/url?q=https://arxiv.org/abs/1604.06737&sa=D&ust=1536845522320000)</span>

<span class="c5">[</span>2] Flunkert, V., Salinas, D. & Gasthaus, <span class="c5">J. (2017).</span> <span class="c5">DeepAR: Probabilistic Forecasting with Autoregressive Recurrent Networks.</span> <span class="c6">[https://arxiv.org/abs/1704.04110](https://www.google.com/url?q=https://arxiv.org/abs/1704.04110&sa=D&ust=1536845522321000)</span>

<span class="c5">[3]</span> <span class="c5">Zhu, L. &</span><span class="c5"> </span><span class="c5">Laptev, N. (2017)</span><span class="c5">Deep and Confident Prediction for Time Series at Uber</span> <span class="c6">[https://arxiv.org/abs/1709.01907](https://www.google.com/url?q=https://arxiv.org/abs/1709.01907&sa=D&ust=1536845522322000)</span>

<span class="c5">[4] Klus, S., Schuster, I., & Muandet, K. (2017). Eigendecompositions of transfer operators in reproducing kernel Hilbert spaces.</span> <span class="c5">Submitted to</span><span class="c5 c1"> Journal of Machine Learning Research</span><span class="c5">.</span> <span class="c6">[https://arxiv.org/abs/1712.01572](https://www.google.com/url?q=https://arxiv.org/abs/1712.01572&sa=D&ust=1536845522322000)</span>

<span class="c5">[5]</span> Song, L., Huang, J., Smola, A., & Fukumizu, K. (2009). Hilbert space embeddings of conditional distributions with applications to dynamical systems. In <span class="c1">Proceedings of the 26th Annual International Conference on Machine Learning</span>.