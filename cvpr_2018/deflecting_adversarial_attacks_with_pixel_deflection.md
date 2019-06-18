# Deflecting Adversarial Attacks with Pixel Deflection

#### Aaditya Prakash, Nick Moran, Solomon Garber, Antonella DiLillo, James Storer


<p align="center">
  <img src="cvpr_2018/img/pixel_def.png" height="400" title="Pixel Deflection">
</p>

### Abstract

This work presents an algorithm which utilizes pixel wise processing to match adversarial images statistics with real image statitics. This, along with wavelet-based denoising operation provides a strong defense against adversarial attacks.

### What it does

Provides a defense against adversarial attacks, which relys on 'pixel deflection' or changing pixels to nearby pixels to provide defense.

### How is it done

1) Get the Roboust Activation Map (which is a proxy of object localization).

2) uniformly sample pixels from the image, with probability of changing inversely proportional to the probability of containing an object.

3) Denoise the image using discrete Wavelet Transform.


### Chief Novelty

A defense method that relys on only switching pixels (with a lot of complexity though). 

### Other Interesting Analysis

* Objects are localized using weakly supervised object localization method.

* For the Discrete Wavelet Transform based denoising, they use Soft Thresholding, and other techniques for adaptive thresholding as well.


**Drawbacks**: 

* The notion that image is flipped to a nearby class is used which is not true for all attacks. (Least Likely attacks etc.)

* Experiments would have been even more interesting if we had highly `L2` normed versions as well.

* "These facts render top-5 accuracy an unsuitable metric for measuring the efficacy of a defense." - Not really a great arguement as at low `L2`, 
  the tested attacks would have lesser damage w.r.t. top-5 accuracy as well.
 
### Impressive Results

<p align="center">
  <img src="cvpr_2017/img/pixel_def_table.png" height="400" title="Defense by Pixel Deflection Table">
</p>
