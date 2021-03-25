+++
date = "2020-10-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "adversarial_learning"
short_description = "Learning models that generalize ove different domains."
title = "Adversarial Learning"

[[participants]]
    name = "Christian Bracher"
    is_member = true
    id = "christian_b"

[[participants]]
    name = "Sebastian Heinz"
    is_member = true
    id = "sebastian_h"

[[participants]]
    name = "Martin Heusel"
    is_member = true
    id = "martin_h"

[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"

+++


### Research Project by [Christian Bracher](/member/christian_b), [Martin Heusel](/member/martin_h), [Sebastian Heinz](/member/sebastian_h) & [Roland Vollgraf](/member/roland_v)

<span style="font-weight: 400;">Deep learning computer vision models, based on our huge archive of fashion images, already empower various customer-facing AI products at Zalando including recommendations, search, and “complete the look”, a product that generates outfits. We currently face two obstacles in applying our models even further: (1) Models that are trained on Zalando’s highly curated shop imagery don't generalize well to other assortments or customer produced content; and (2) Model performance is tainted by spurious correlations with confounding but irrelevant sources of information inside the Zalando image catalog. We aim to overcome both obstacles with the help of methods from adversarial learning.</span> 

![recommended articles](img/image2.png) 

Article images from different sources 

### Implementation Challenges
 <span style="font-weight: 400;">Adversarial learning tasks can be formulated with the help of two-player games. Here the first player’s goal is to predict a certain attribute (like the image source), while the second player’s goal is to sabotage the first player. Mathematically, this corresponds to solving saddle point optimization problems. As adversarial learning following this strategy is notoriously unstable (see the figure below for the particular challenge of “orbiting”), we plan to improve its training behaviour by refining optimization algorithms exploring 2</span>

<span style="font-weight: 400;">nd</span> 
<span style="font-weight: 400;">order methods as well as insights from image GANs. We also plan to approach the problem by finding adversary objectives (like MMD, meta learning) that avoid the need of solving saddle point optimization problems, without unduly affecting classification ability.</span> 

![“Orbiting” of weight traces (sinusoidal graphs) implies lack of convergence.](img/image3.png) 
“Orbiting” of weight traces (sinusoidal graphs) implies lack of convergence. 

### Learning-to-Forget Example
 <span style="font-weight: 400;">We have an article embedding which encodes, in particular, the type of fabric, season, targeted gender and age, the color as well as the brand of a fashion item:</span> [<span style="font-weight: 400;">Fashion DNA</span>](../../fashion_dna/fashion_dna)<span style="font-weight: 400;">. Via adversarial learning, we trained a model on top of Fashion DNA with the task to forget all article properties except for color and pattern. Examples of neighborhoods with respect to the resulting article embedding are shown below.</span> 
 ![LSTM-based network](img/image1.jpg) 
 ![recommended articles](img/image4.jpg)