# Universal Adversarial Perturbations

#### Seyed-Mohsen Moosavi-Dezfooli, Alhussein Fawzi, Omar Fawzi, Pascal Frossard


<p align="center">
  <img src="cvpr_2017/img/uap.png" height="400" title="UAP Image">
</p>

### Abstract

This work introduces a completely new paradigm of attacking neural networks, 
where a single perturbation is used to fool the model in a image agnostic fashion.

### What it does
The authors provide an algorithm to generate universal adversarial perturbations (UAP).
 
### How is it done
The UAP is formed by accumulation of `DeepFool` perturbations over a subset of training 
images (with a norm restriction).

### Chief Novelty
Discovering the existence of such UAPs. A single noise which can flip labels on all images (approximately)!

### Other Interesting Analysis

* Show the existence of sink classes: A few classes to which most of the images flip too.

* Present supporting argument for the existence of a subspace of low dimension that contains
most normal vectors to the decision boundary in regions surrounding natural images; i.e.
the normal vectors of learnt decision boundaries may be correlated (Hence UAPs can exist). 


**Drawbacks**: The performance drops strongly as amount of data used for generation is decreased. 
But the author address this issue in future work! 

### Impressive Results

The fooling rates across different image classification models. Each row corresponds to the 
network used for generating a UAP, and each column corresponds to the network on which fooling
rate is evaluated.

<p align="center">
  <img src="cvpr_2017/img/uap_table.png" height="400" title="UAP Table">
</p>