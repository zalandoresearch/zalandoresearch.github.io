+++
date = "2017-08-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "fashion_mnist"
short_description = "Fashion MNIST"
title = "Fashion MNIST"
[[participants]]
    name = "Kashif Rasul"
    is_member = true
    id = "kashif_r"
[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"

+++



### Research Project by [Kashif Rasul](/alumni/kashif_r), Han Xiao (ex-member) & [Roland Vollgraf](/alumni/roland_v)

Fashion-MNIST is a dataset of Zalando's article images consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. Fashion-MNIST is intended to serve as a direct drop-in replacement of the original MNIST dataset for benchmarking machine learning algorithms. ![fashion-mnist-sprite](img/fashion-mnist-sprite.png) 

#### Why is this of interest for the scientific community?
The original [MNIST dataset](http://yann.lecun.com/exdb/mnist/) contains a lot of handwritten digits. People from AI/ML/Data Science community love this dataset and use it as a benchmark to validate their algorithms. In fact, MNIST is often the first dataset they would try on. _"If it doesn't work on MNIST, it won't work at all"_, they said. _"Well, if it does work on MNIST, it may still fail on others."_ Fashion-MNIST is intended to serve as a direct drop-in replacement for the original MNIST dataset to benchmark machine learning algorithms, as it shares the same image size and the structure of training and testing splits.

###### ![benchmark](img/benchmark.gif)

Seriously, we are talking about replacing MNIST. Here are some good reasons:

*   MNIST is too easy. Check out [our side-by-side benchmark.](http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/) and ["Most pairs of MNIST digits can be distinguished pretty well by just one pixel"](https://gist.github.com/dgrtwo/aaef94ecc6a60cd50322c0054cc04478)
*   MNIST is overused. Check out ["Ian Goodfellow wants people to move away from mnist."](https://twitter.com/goodfellow_ian/status/852591106655043584)
*   MNIST can not represent modern CV tasks. Check out ["François Chollet: Ideas on MNIST do not transfer to real CV."](https://twitter.com/fchollet/status/852594987527045120)

**GitHub:**

[Find detailed information and the data set on GitHub](https://github.com/zalandoresearch/fashion-mnist)