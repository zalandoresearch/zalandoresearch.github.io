+++
date = "2021-01-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "fdna"
short_description = "An Introduction to Fashion DNA"
title = "Improving Fashion Item Encoding and Retrieval"
[[participants]]
    name = "Christian Bracher"
    is_member = true
    id = "christian_b"

[[participants]]
    name = "Sebastian Heinz"
    is_member = true
    id = "sebastian_h"
+++

#### Team members:
* [Christian Bracher](../../../member/christian_b)
* [Sebastian Heinz](../../../member/sebastian_h)

Unlike a brick-and-mortar department store, online retailers like Zalando must use digital representations of their offerings to entice customers. Traditionally, this takes the form of information stored in a catalog database, which collects categorical properties (tags), numerical descriptors (e.g., prices), and images of the items. Although this information is curated by in-house experts, assignments are often subjective (what makes a dress ‘dark red,’ or ‘leisure’?), and article imagery is highly stylized. It is also by no means complete. More importantly, there is no straightforward relation between these article attributes, and the properties individual customers actually care about:

* Does it fit?
* How does it feel wearing?
* Does it suit my style?

### Fashion DNA

To make the properties of a fashion item more accessible, we collect the array information in the catalog and map it into an abstract mathematical linear space, the fashion space. There, the item is represented by a vector, its Fashion DNA. Unlike the catalog data, Fashion DNA is a fundamentally geometrical representation:  The similarity between two articles is encoded by their distance in fashion space, while article properties (is it blue? Is it a dress? Is it offered by Nike? Does customer #1,234,567 like it?) are associated with specific directions in this space.

For instance, the mosaic below is based on a t-SNE embedding that groups fashion articles by their distance:

![t-SNE map of fashion articles, based on Fashion DNA](img/tsne_map.mosaic.detail.jpg)

This example arranges dresses along a slice of fashion space that connects red to blue (horizontal) and striped to dotted (vertical):

![Dots to stripes transition](img/dresses.png)

We may also define a similarity measure between fashion attributes, based on the angle between their associated directions. For instance, the brand *Desigual* ® is associated with the pattern attributes paisley, colorful, and floral.  Likewise, we can find similar brands, or identify customers whose personal style axis in fashion space aligns with the brand.

### Applications

Linear embeddings yield access to a powerful arsenal of inference methods in the fashion universe. Generally, Fashion DNA encodings are extracted as hidden activations in a feedforward deep neural network (DNN) that is trained on a relevant target, e.g., prediction of brands and silhouettes from images, mapping images to fashion items, or prediction of customer sales from attributes and images. The resulting Fashion DNA is correspondingly optimized for different tasks. For instance, the latter setup naturally leads to an enhanced collaborative filtering recommender system for fashion.

In addition to the choice of target data, we may select which input data to feed, and we have a wide latitude of neural network architectures to transform the data. Hence, we can experiment with Fashion DNA models that are tailored to specific use cases. A few prospective applications are:

#### Image Tagging

Here, the idea is to train a neural network on a set of images for an item, with the goal of predicting catalog tags (like brand, color, silhouette, etc.).  During inference, feeding item images into the trained network results in a vector of probabilities for each tag, providing estimates for target groups, brand membership, color, pattern, material, etc.:

There are a variety of applications beneficial to Zalando’s business, e.g.,

![Shoe analysis](img/tagging_new.jpg)

* AI tagging support – tagging new additions to the online shop is a resource-intensive, error-prone, and subjective task. The algorithm can suggest tags and identify labeling mistakes and omissions.
* Finding fashion trends – analyzing images posted by trendsetters, influencers, and shows, one could detect fashionable styles early on.
* Assessing competitors’ assortments – applied on crawled images, the method can provide continuously updated insights into the strategies of other players in the online fashion sector.

#### Information Synthesis, Inference, and Uncertainty
Fashion information often is embedded in an implicit context that is easy to disentangle for a human observer with daily life experience, but presents a difficult challenge to machine learning algorithms. For instance, images may depict a model wearing a variety of fashion articles in front of a structured background, or detailed views of an item (seams, tags, brand logos, etc.) that are of particular interest to customers. It doesn’t take much effort for a human to focus on a specific element of the model outfit (the image segmentation problem), or to imagine the three-dimensional appearance of an article from a few two-dimensional snapshots.

The ease at which humans go about these tasks suggests that our internal representation “engine” is not only able to aggregate the information, but also can infer missing attributes and handle uncertainty. Conventional feed-forward neural network architectures are not well equipped for the purpose, while more recent probabilistic models like variational autoencoders form a basis for developing a more powerful representation scheme.

Still, even minor tweaks like changing the loss function can already render Fashion DNA much more resilient to the presentation of an item, as the map below demonstrates:

![Shoe analysis](img/hinge_loss.tsne.png)

Note that the model assigns similar encodings to very different views of an article (visible as clusters in the map), while still being able to extract abstract attributes like brand, silhouette, etc., with good precision.  Such Fashion DNA is a useful substrate for our efforts to solve the street-to-shop task, matching fashion items depicted in real-life images to items in the online store.