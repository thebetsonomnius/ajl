---

title: "Intelligence as Requisite Work (stub)"

date: 2023-04-20

---

<!-- more -->

IQ is an empirically derived variable. Many people are against it as a metric for precisely this reason. Let's try to fix that.

From first principles, we might define an IQ as some strictly decreasing function of the average amount of work a neural network must do to account for novel data. We can define work as the "distance" between a neural network's parameters before and after accounting for some novel data. In deep learning, that distance function should be some measure of the change in geometry of the output space\* of the neural network, within the old data distribution's support. The canonical family of techniques for measuring the latter is [centered kernel analysis](https://arxiv.org/pdf/1905.00414.pdf). This operationalization of IQ is pleasing due to the ease with which it can be evaluated on neural networks of arbitrary size. It also comports with the observed properties of neural networks, namely that they get "smarter" with more parameters and data.

