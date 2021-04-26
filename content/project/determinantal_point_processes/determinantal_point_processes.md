+++
date = "2018-09-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "determinantal_point_processes"
short_description = "Determinantal Point Processes"
title = "Determinantal Point Processes"

+++

### Research Project by Leonidas Lefakis (ex-member)

Chic, shocking, trendy, or casual, Fashion must never be monotonous. As such, diversity plays a central role in fashion. At Zalando we research such topics, focusing on elegant mathematical models named Determinantal Point Processes (DPPs) that capture notions of both relevance and diversity in a principled manner.

Defined over a fixed ground set $\Upsilon$, for example the articles in the Zalando catalogue, DPPs define a distribution over subsets of $\Upsilon$. By encoding negative correlations between items in the set via a kernel matrix, a DPP will assign higher probability to subsets that are diverse. At the same time DPPs can in parallel encode the relevance of each item to a specific task, via a relevance score for example, thus allowing for a trade-off between the two aspects of the task.

DPPs find many applications within Zalando, Two such cases are Recommendations and Search. In Recommender Systems, it easy to become trapped in a scenario where the system recommends the same or very similar articles simply because they are individually deemed relevant. DPPs allows the system to recommend a collection of items which is diverse, while retaining relevance, thus attempting to capture different aspects of a customer’s taste and preferences. In Figure 1 we show the two different sets of recommendations, one using only a relevance score and one using a DPP to infuse diversity (leveraging [Fashion DNA](../../fashion_dna/fashion_dna/)).  


![image1](img/image1.png)

Similarly, a search query can return a list of items that are very similar to each other simply because they are deemed relevant to the query without taking into account the inter-relationships between the items. In a related scenario, the items may well only capture one meaning of the search query when ambiguous terms are present. DPPs help mitigate such issues by diversifying the retrieved items. In Figure 2 we present two different search results, one drawn from a DPP and the other taking only relevance into account, which highlight these differences.

![image2](img/image2.png)

As mentioned above, these two scenarios are just some of the cases where DPPs find applicability. Research is ongoing both on applying DPPs to various tasks as well as developing novel algorithms for both learning and inference with DPPs.
