# Adversarial Defense Through Network Profiling Based Path Extraction

#### Yuxian Qiu, Jingwen Leng, Cong Guo, Quan Chen, Chao Li, Minyi Guo, Yuhao Zhu

<p align="center">
  <img src="cvpr_2018/img/path_extraction_defense.png" height="400" title="Network profiling based path extraction.">
</p>

### Abstract
The authors establish that the effective path of activations is different for adversarial and normal samples. 
Hence, they propose to use class specific aggregation of 'effective-path of activation' to yield discriminating 
statistics.

### What it does
Based on extracted "effective path", it detects if the image is clean or adversarial.

### How is it done

* **Profiling**: Each layer has a set of effective activations. For each effective activation, the minimal set of 
connected activations in the previous layer which contribute more than a fixed ratio of the effective activation are 
taken as effective activations in the previous layer.

* **Detection**: Image Class path similarity, which indicates how many synapses in the image’s effective path come 
from the predicted class’s effective path. Use the similarity scores for the Rank 1 and Rank 2 classes with various 
ML techniques (Random Forests, Linear Modelling) for detecting adversarial samples.


### Chief Novelty
The proposed path profiling, without any retraining of the network, achieves better than SOTA adversarial attack 
detection success rate.

### Other Interesting Analysis

* Perform similarity analysis and find the phenomenon (which they) called "path specialization" that different classes 
activate distinctive portions of the neural network in the inference task.

* Validate that the class specific aggregated path is sparse and critical for the inferred outcome.

* Also useful for unrecognizable samples. 

**Drawback** :  

* Some of the critical analysis are performed in smaller datasets, with slighly unclear meta data (which dataset etc.)

* Some of the critical analysis is missing for large networks such as ResNet-152.

### Impressive Results


<p align="center">
  <img src="cvpr_2018/img/path_extraction_defense_table.png" height="400" title="Results for Network profiling based 
  path 
  extraction">
</p>
