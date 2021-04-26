+++
date = "2016-12-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "forecasting_the_customers_preference"
short_description = "Forecasting the customer’s preference"
title = "Forecasting the customer’s preference"
[[participants]]
    name = "Christian Bracher"
    is_member = true
    id = "christian_b"

[[participants]]
    name = "Sebastian Heinz"
    is_member = true
    id = "sebastian_h"
    
+++

### Research Project by [Christian Bracher](/member/christian_b) & [Sebastian Heinz](/member/sebastian_h)
We study time series of interactions of articles (fashion items) with customers. Our focus lies on personalized data, meaning, that each time series collects data for a single customer only. Examples include the customer’s purchase history as well as their click chain through the product detail pages in the shop. Our aim is to build a method which takes the past of a time series as input and effectively forecasts future events – the task of a recommender system. In other words, we want to identify customer preferences (their “style”), and follow their changes through time. Such a method may have a big impact on personalizing the customer shopping experience, and we collaborate with Zalando’s recommendation team on that topic.

#### The Fashion DNA model
Our key idea is to map an article to a numerical representation, its so-called Fashion DNA. This vector encodes the article’s curated information including brand, silhouette, etc., as well as visual data, and is extracted as activations in a hidden layer of a deep neural network. For the recommendation use case, the network is trained on the sales record, akin to collaborative filtering. The Fashion DNA created in this way, however, is agnostic about the sequence of purchases, as it does not take temporal information into account.

#### Purchase prediction with LSTMs
To introduce temporal order, we turn to a network architecture that is designed to process sequential data, and “memorize” patterns in internal states. We use a Long Short-Term Memory (LSTM) layer which was designed to simultaneously deal with phenomena on different time scales. Training the network involves feeding sequences of customers’ past purchases, with bought items represented by their Fashion DNA, and the goal is to predict the style preference of the customers as it changes over time. The basic processing steps of our model are sketched below:

![](img/lstm_sketch-1024x411.jpeg)
_Figure 1. LSTM-based network_

Ideally, in addition to static customer preferences (like favorite colors), the model will now be able to recognize secular drifts such as fashion trends and changing personal circumstances, as well as periodic influences like seasons. The figure below indicates what the model recommendations for a sample customer in the fall/winter season may look like.
![](img/cold_weather_reco-1024x296.jpeg)
_Figure 2. Recommended articles._

More details can be found in our paper [An LSTM-Based Dynamic Customer Model for Fashion Recommendation](http://ceur-ws.org/Vol-1922/paper9.pdf).

#### Circumventing the “cold-start problem”
Standard recommendation algorithms that rely only on purchase information (like collaborative filtering) commonly suffer from the cold-start problem: New items have no purchase records and cannot be matched to customers. Because our approach is anchored to curated fashion content via Fashion DNA, we are largely able to avoid this shortcoming; our algorithm will issue meaningful recommendations for articles even as they just entered the shop, and present new fashion items much earlier to interested customers.

#### Next-click prediction
A click chain contains customer-article interactions of different event types: “add to cart” and “order” are two examples. Event types show very different levels of information. While an order event speaks for a strong affinity between customer and article, the browsing of a product detail page alone does not. We train a variant of the above model to handle the different event types. The goal is to recommend fashion items which reflect the long-term as well as the short-term interest of the customers.
