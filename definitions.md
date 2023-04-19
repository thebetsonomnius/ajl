---
title: Definitions
permalink: /definitions/
---

## zemlems
A zemlem is a ZettascalE MultimodaL Model (the 2nd e is inserted for phonetic consistency). The replacement of language
with multimodal is for posterity's sake - some models are language-only, and some aren't, but it follows from the
[circuit co-evolution theory](#circuit-coevolution-theory) that Transformer generalization increases with the
diversity of the training data. It is therefore safe to assume that in several years' time, LLMs will be completely
replaced by LMMs. Zettascale refers here to the number of floating point operations required to train the model. With 
the exception of PaLM 540B and likely GPT-4-vision (which are [yemlems](#yemlems)), most of the largest models in 
existence today are zemlems. They are trained on clusters with theoretical max throughput of 1-25 exaFLOPS.

## yemlems
A yemlem is a YottascalE Multimodal Model (the 2nd e is inserted for phonetic consistency). The replacement of language
with multimodal is for posterity's sake - some models are language-only, and some aren't, but it follows from the
[circuit co-evolution theory](#circuit-coevolution-theory) that Transformer generalization increases with the
diversity of the training data. It is therefore safe to assume that in several years' time, LLMs will be completely
replaced by LMMs. Yottascale refers here to the number of floating point operations required to train the model. This 
class is quite sparsely populated at the moment. The only models publicly stated to fall in this class are PaLM 540B 
(per the training wall-clock time stated by Google multiplied by the stated realized FLOP throughput of the dual TPUv4 pods),
and GPT-4-vision (per Sam Altman's public comments at MIT on the dollar-cost of training the GPT-4 family).

## the pure language limit
Per calculations based on the [separation rank of decoder-only Transformers](https://arxiv.org/pdf/2105.03928.pdf), and
the hypothesized amount of high-volume or high-quality tokens on the internet, there are fundamental limits to the
compute and parameter count scaling laws of LLMs. If one assumes the scaling laws derived from the separation rank
figures linked to in the previous sentence, the largest LLM one can profitably train is between 1T-1.3T parameters. I
presume a constant vocabulary size of ~32K, due to the theoretical and [apparently practical](https://uploads-ssl.webflow.com/60fd4503684b466578c0d307/61138924626a6981ee09caf6_jurassic_tech_paper.pdf) improvements in generalization at 
the expense of inference speed that come from a narrower vocabulary.

## circuit coevolution theory
Transformers learn circuits, rather than key-value stores. While it is true that at initialization time Transformers are closer in parameter space to
memorization-based solutions than to generalizing solutions, it turns out that the former are not located in
homogeneous loss basins. What that means is that, given sufficient training iterations and a sufficiently large i.i.d 
sampling of the data distribution, Transformers will find generalizing solutions. Such behavior is referred to as
grokking. Mathematically rigorous investigations of this phenomenon remain limited to toy problems like the learning of
k-sparse boolean parities, but the empirical literature is quite clear. Generalization performance, formalized as the rate at
which Transformers progress from the memorizing solution to the generalizing solution, is determined by the diversity
of circuits present in the network close to initialization time. Further explanation of this phenomenon is beyond the
scope of the definitions page. See the accompanying [post](https://ajl.bio/2023/04/18/initiation.html) for a proper and
rigorous exposition.

