
+++
date = "2016-12-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "generative_models_research"
short_description = "Texture Modelling with the Spatial GAN"
title = "Generative Models Research"

[[participants]]
    name = "Nikolay Jetchev"
    is_member = true
    id = "nikolay_j"

[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"

+++

### Research Project by Urs Bergmann (ex member),  [Nikolay Jetchev](/member/nikolayj) & [Roland Vollgraf](/member/roland_v)

<span style="font-weight: 400;">The overarching goal of this project is to advance the field of generative modeling, i.e. to build methods that learn complex probability distributions. In particular, we focus on generative adversarial networks (GANs), a relatively new technique that has shown impressive results in purely data-driven modeling of images.</span>


_Texture created by Zalando Research method:_
![texture created by Zalando Research method](img/Z_TEX10-e1481797528740.png)


<span style="font-weight: 400;">We have developed a novel method for texture synthesis called Spatial-GAN, or SGAN. Our method has the following features which make it a state of the art algorithm for texture synthesis:</span>

*   <span style="font-weight: 400;">high image quality of the generated textures</span>
*   <span style="font-weight: 400;">very high scalability w.r.t. the output texture size</span>
*   <span style="font-weight: 400;">fast real-time forward generation</span>
*   <span style="font-weight: 400;">the ability to fuse multiple diverse source images in complex textures.</span>


_Zalando box packaging:_
![Zalando box packaging by Zalando Research](img/zalando-produkte-2sp2x.png)


<span class="s1">Our paper has been accepted at the NIPS 2016 adversarial learning workshop:</span>

<span class="s2">[https://arxiv.org/abs/1611.08207](https://arxiv.org/abs/1611.08207)</span>

<span class="s1">and follow-up work has been accepted to the International Conference for Machine Learning 2017:</span>

<span class="s2">[https://arxiv.org/abs/1705.06566](https://arxiv.org/abs/1705.06566)</span>

#### Videos:

<span class="s1">The video shows how we can learn a large texture model from an example painting (by Juan Miro) and use it to dynamically morph and paint the Zalando logo.</span>

[![video](https://img.youtube.com/vi/qyfEZ11uFNg/0.jpg)](https://www.youtube.com/watch?v=qyfEZ11uFNg)

We could get as a texture the satellite image of the city of Barcelona, and then generate a gigantic random city texture with the statistics of the Barcelona image, In our paper we examine that example in detail and show the superior performance of our approach compared to other techniques.

[![video](https://img.youtube.com/vi/HaFhfDzChUk/0.jpg)](https://www.youtube.com/watch?v=HaFhfDzChUk)

If you want to generate infinite textures yourself,  check out our method on github:
*   [<span style="font-weight: 400;">https://github.com/zalandoresearch/spatial_gan</span>](https://github.com/zalandoresearch/spatial_gan) <span style="font-weight: 400;">and</span>
*   [<span style="font-weight: 400;">https://github.com/zalandoresearch/psgan</span>](https://github.com/zalandoresearch/psgan)