# Exact Adversarial Attack to Image Captioning via Structured Output Learning with Latent Variables

#### Yan Xu∗, Baoyuan Wu∗, Fumin Shen, Yanbo Fan, Yong Zhang, Heng Tao Shen, Wei Liu

<p align="center">
  <img src="cvpr_2018/img/captioning.png" height="400" title="Attacking Image Captioning">
</p>

### Abstract

This work introduces two novel approaches to fool deep learning systems using non-deep optimization methods. Specifically, the proposed method is utilized to fool captioning systems and yield target partial caption from given images by adding imperceptible perturbations.

### What it does

The proposed optimzation crafts image specific perturbations which can yield Target partial captions when added to caption generation model's input.

### How is it done

Firstly the problem is formulated as  structured output learning problem with latent (hidden) variables.

Then, Generalized Expectation maximization and Strutural SVMs with latent variables are utilized to generate perturbations which maximize probability of the target partial caption.   

### Chief Novelty

Attacking Captioning systems for target partial captions. Additionally utilizing GEM and SVMs for perturbation optimization (a departure from typical gradient based methods Momentum etc.). 

### Other Interesting Analysis

The authors show untargetted attacks as well, where seeing the grammar fail is very interesting. 

**Drawback** :  

* The Target captions are from the caption dataset itself. Can it work for any random caption?

### Impressive Results

Imp Metric: SR stands for success rate of the attack.

<p align="center">
  <img src="cvpr_2018/img/captioning_table.png" height="400" title="Attacking Image Captioning Results">
</p>
