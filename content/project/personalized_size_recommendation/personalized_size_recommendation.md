+++
date = "2018-09-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "personalized_size_recommendation"
short_description = "Personalized Size Recommendation"
title = "Personalized Size Recommendation"
+++

### Research Project by Abdul-Saboor Sheikh (ex-member)  & Urs Bergmann (ex-member)
Have you ever wondered what would be the best fitting size of a clothing item that you would like to order online? You may have an idea about the size you generally wear, but this piece of clothing perhaps comes in a different size system or maybe it is a style or category that you have not worn before. Then apart from your own preferences, there may be other factors (such as brand, design, material, manufacturing, etc.) that may as well come into play when determining the right size that would give you the best fit and feel.

Zalando has a lot of customer order and purchase data that spans over a huge assortment of fashion articles. In this project our aim is to benefit from this wealth of information to develop a personalized size recommendation service for our customers.

In spite of having a lot of data, a key challenge with personalization is sparsity – an individual customer often only has a handful of articles in their purchase history. To alleviate this, we are focused on developing models that can leverage size and fit relevant information across individual customers to improve personalized recommendations. Our system is context-aware, where a context may be defined based on attributes that are pertinent to a customer-article pair. The core idea behind the system is to develop a unified mapping scheme such that it allows for both customers and articles to be implicitly projected and compared in a semantic-free (latent) feature space. As illustrated in the schematic below, given such a mapping scheme a customer projected into the hidden space can be aligned with size-specific mappings of an article for making personalized size recommendations.

![image12](img/image12.png)

What machine learning methods do we use? In this project we have explored the potential of Bayesian modeling as well as deep learning. Bayesian theory provides us with a principled framework for combining beliefs about missing or sparse information with noisy observations. A Bayesian size recommendation model [1] appeared at RecSys 2018. On the other hand, in scenarios with ample data and relatively low signal to noise ratio, deep learning has been shown to be empirically very effective in approximating highly non-linear (unknown) functions. Our work [2] that proposes a deep learning based approach for personalized size and fit recommendation has achieved state-of-the-art results on publicly available, as well as internal, datasets for size recommendation. The work has been accepted at RecSys 2019.

#### References
[1] A Hierarchical Bayesian Model for Size Recommendation in Fashion. Guigourès, R., Ho, Y. K., Koriagin, E., Sheikh, A. S., Bergmann, U., & Shirvany, R., RecSys 2018.

[2] A Deep Learning System for Predicting Size and Fit in Fashion E-Commerce. Sheikh, A. S., Guigoures, R., Koriagin, E., Ho, Y. K., Shirvany, R., Vollgraf, R., & Bergmann, U., RecSys 2019 (to appear).

