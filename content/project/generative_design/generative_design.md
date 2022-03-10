+++
date = "2018-01-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "fashion_renderer"
short_description = "Generative Design"
title = "Generative Fashion Design"
[[participants]]
    name = "Gökhan Yildirim"
    is_member = true
    id = "gokhan_y"

+++

#### Team members:
* [Gökhan Yildirim](/alumni/gokhan_y)

What is the fastest way to visually communicate a new design? Searching for similar-looking clothes? Drawing a sketch? Or creating a 3D representation on a computer program? Although all of them are viable solutions, they are quite time consuming.

At Zalando, we target an agile design process that combines invaluable human experience with the power of Machine Learning (ML). In particular, we do research on novel ways to use generative models in fashion design for rapid visualizations and prototyping. One such ML model is the Generative Adversarial Network (GAN).

GAN is a deep learning architecture that learns the real data distribution in an adversarial setting. In our case, the real data correspond to the images of the articles in Zalando’s inventory. A GAN, which is trained on these images, can generate realistic-looking garment designs.

In its original formulation, GANs only allow us to sample a generated image of a random article. However, in the context of fashion design, we want to control the clothing attributes, such as color, texture, and shape. In addition, it is desirable to disentangle the effects of these attributes, so that each aspect of the design can be independently manipulated as shown below:

![Example generation](img/image42.png)

IIf you’re interested in more details, check out our paper on generative fashion design and disentangling topic (presented at KDD-2018 AI for Fashion Workshop):

[Disentangling Multiple Conditional Inputs in GANs](https://www.google.com/url?q=https://arxiv.org/abs/1806.07819&sa=D&ust=1536846697988000)

Here are some example designs that were created by our generative model:

Controlling Color:

![Example generation](img/image16.png)

Controlling texture:

![Example generation](img/image31.png)

Controlling shape:

![Example generation](img/image24.png)