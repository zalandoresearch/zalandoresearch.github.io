+++
date = "2019-06-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "swarm"
short_description = "Learning Permutation Equivariant Functions"
title = "SWARM"
[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"
+++

### Research Project by [Roland Vollgraf](/alumni/roland_v)

**SWARM Layers** are a new approach to build powerful learnable set functions. These are multi-variate function over a set (or population) of entities that exhibit permutation equivariance or invariance, i.e. these functions are explicitly agnostic to the order of entities. **Architecture** Building bocks for **SWARM Layers** are **SWARM Cells**. These are modified LSTM cells that are augmented with an additional input. Together with the network input _x_ and the previous hidden state _h_ they also receive an input _p_ which resembles pooled information over the whole population. ![SWARM Cell](img/swarm_cell.png) The same SWARM cell (S), shared over the whole population of entities, is executed repeatedly for a number of iterations, where the number of iterations is a model hyper parameter. The pooling operation (P) can be simple average pooling, or any other low level set-invariant function. To build a SWARM based Transformer-like architecture, causal average pooling is used (thereby giving up the strict permutation equivariance, for details see the paper). The iterations plus pooling together with an output fully connected layer form the SWARM Layer ![SWARM Layer](img/swarm.jpg) SWARM Layer can provide state-of-the-art performance in various applications **already with single layer architectures**. They can, of course, also be stacked to multi-layer architectures or can be combined with other set-equivariant functions. In particular, because of their permutation-equivariant semantics, they can be used as a direct replacement for self attention blocks in various architectures. In the recently proposed powerful Transformer architectures, they can lead to significantly smaller models, as we have shown in the paper [Learning Set-equivariant Functions with SWARM Mappings](http://arxiv.org/abs/1906.09400).   SWARM layer can be trained, for example,  to perform amortized clustering tasks, like in this example: ![amortized_clustering](img/amortized_clustering-e1570808864909.png) Here, the SWARM layer sees a population of points at once and simultaneously assigns them to one out of ten possible clusters. The grey shaded areas indicate how confident is about it. A PyTorch implementation of SWARM can be found on Github at [https://github.com/zalandoresearch/SWARM](https://github.com/zalandoresearch/SWARM)