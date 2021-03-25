+++
date = "2018-09-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "shop_the_look_with_deep_learning"
short_description = "Shop the look with deep learning"
title = "Shop the look with deep learning"

+++

### Research Project by Julia Lasserre (ex-member)
Have you ever seen a picture on Instagram and thought “oh wow, I need these shoes”? or been inspired by your favourite fashion blogger and looked for similar products (for example on Zalando)? Visual search for fashion, the task of identifying fashion articles in an image and finding them in an online store, has been the subject of an ever growing body of scientific literature over the last few years, and has been offered by many fashion stores.

Many modern models treat visual search as a domain transfer problem, and use what is referred to as a siamese approach: query fashion images and products are processed in different branches, a representation is learnt for each branch and a match is learnt between these two domains, as shown in Figure 1a. We follow a similar approach, however for us the product representation is pre-learnt and fixed, using our internal [FashionDNA](../../fashion_dna/fashion_dna). Figure 1b illustrates this difference by showing the shortened leg on the article side (the right side).

<img style="width:100%;" alt="bla" src="img/image4.png" />

![image4](img/image4_.png)
a) Popular siamese approach. 

![image21](img/image21_.png)
b) Our approach: article features f(A) are fixed and given by FashionDNA.

_Figure 1: Difference between our approach and the popular one. I is the query image, A the article, f(I) the image representation, f(A) the article representation. The query article matching module uses the query image representation and the article representation to predict a match between the two._

![image6](img/image6.png)
_Figure 2: Examples of images in our dataset. Image types (a-d) are query images featuring models, image type (e) is used to train FashionDNA._

Unfortunately, an overwhelming majority of our fashion images have standardised clean backgrounds as shown in Figure 2, which means we have to think of a work around to learn how to handle realistic query images.

Using mostly publicly available datasets, such as Chictopia 10K, we design and train Street2Fashion, a U-net-like segmentation model that can find the person in the image and simply replace the background with white pixels.

We use Street2Fashion as a preprocessing step, and build Fashion2Shop, a modeth the same architecture as in Figure 1b, but trained on segmented images. We refer to the full pipeline described in Figure 3 as Street2Fashion2Shop. In practice, a query fashion image is processed by the segmentation model to remove the background, and can then go through the matching model described above to be matched with appropriate products.

![image11](img/image11.png)
_Figure 3: Street2Fashion2Shop. The query image (top row) is segmented by Street2Fashion, while FashionDNA is run on the title images of the products in the assortment (bottom row) to obtain static feature vectors. The result of these two operations forms the input of Fasion2Shop which handles the product matching._

Our working scenario is to retrieve the categories blazers, dresses, jumpers, shirts, skirts, trousers, t-shirts and tops. Figure 4 shows results obtained using Street2Fashion2Shop.

![image5](img/image5.png)
(a) Random examples of Zalando products retrieval using query images from LookBook [2].

![image3](img/image3.jpeg)
(b) Random examples of Zalando products retrieval using query images from street shots.

_Figure 4: Qualitative results on external datasets. For each query image, the query image is displayed on the very left, followed by the segmented image and by the top 50 product suggestions. Better viewed with a zoom._

The details of this work are available in [1] and [3].

#### References

[1] J. Lasserre, K. Rasch and R. Vollgraf. Studio2Shop: from studio photo shoots to fashion articles. International Conference on Pattern Recognition Applications and Methods (ICPRAM), 2018.

[2] D. Yoo, N. Kim, S. Park, A.S Paek and I. Kweon: Pixel-level domain transfer. European Conference on Computer Vision (ECCV), 2016.

[3] J. Lasserre, C. Bracher and R. Vollgraf. Street2fashion2shop: Enabling visual search in fashion e-commerce using studio images, International Conference on Pattern Recognition Applications and Methods, 3-26, 2018

