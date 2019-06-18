# Defense against Adversarial Attacks Using High-Level Representation Guided Denoiser

#### Fangzhou Liao*, Ming Liang∗, Yinpeng Dong, Tianyu Pang, Xiaolin Hu, Jun Zhu.


### Abstract

This work presents High-Level representation guided denoiser (HGD) which 'denoises' adversarial images and recovers correct predictions.This work won the first place for defense against adversarial attacks.

### What it does

Learn a denoise based on the high-level representation difference between normal and adversarial images. This denoise is then used as a defense mechanism against adversarial attacks.

### How is it done

First, DUNET is proposed as a improvement over Normal Denoising auto encoders, which takes the image as input and predicts the delta required to denoise the image.

The network is trained to reduce the distance between the normal and adversarial representations at last convolution or logits layer.

### Chief Novelty


### Other Interesting Analysis

* HGD trained with one target model is usable for other models as well.

* It denoises adversarial samples of unseen classes as well.

**Drawback** :  

* Attacks like CW and PGD not considered.

* Given the stark performance difference between Denoising Autoencoders and DUNETs, results of DAE with proposed losses would be of interest.

### Impressive Results


<p align="center">
  <img src="cvpr_2018/img/guided_denoiser_table.png" height="400" title="Table for Guided Denoiser.">
</p>
