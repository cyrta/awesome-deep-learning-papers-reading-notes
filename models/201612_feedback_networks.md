# Feedback Networks

by [@**zamir\_ar**](https://twitter.com/zamir_ar) et al

[https://arxiv.org/abs/1612.09508](https://arxiv.org/abs/1612.09508) _Submitted on 30 Dec 2016 _

#### Notes

* Good to remember for classification with a taxonomy.
* Uses ConvLSTMs.
* Creates different representations than feedforward nets. Possible smaller models with similar accuracy.

#### 

#### Abstract

> Currently, the most successful learning models in computer vision are based on learning successive representations followed by a decision layer. This is usually actualized through feedforward multilayer neural networks, e.g. ConvNets, where each layer forms one of such successive representations. However, an alternative that can achieve the same goal is a feedback based approach in which the representation is formed in an iterative manner based on a feedback received from previous iteration's output.
>
> We establish that a feedback based approach has several fundamental advantages over feedforward: it enables making early predictions at the query time, its output naturally conforms to a hierarchical structure in the label space \(e.g. a taxonomy\), and it provides a new basis for Curriculum Learning. We observe that feedback networks develop a considerably different representation compared to feedforward counterparts, in line with the aforementioned advantages. We put forth a general feedback based learning architecture with the endpoint results on par or better than existing feedforward networks with the addition of the above advantages. We also investigate several mechanisms in feedback architectures \(e.g. skip connections in time\) and design choices \(e.g. feedback length\). We hope this study offers new perspectives in quest for more natural and practical learning models.

![](https://pbs.twimg.com/media/DZyfRQpX0AENqbm.jpg)

