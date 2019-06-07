# Art of singular vectors and universal adversarial perturbations

#### Valentin Khrulkov, Ivan Oseledets


<p align="center">
  <img src="cvpr_2018/img/sv_uap.png" height="400" title="Defense Against UAP Image">
</p>

### Abstract

This work proposes a new approach for crafting UAPs, using `(p,q)`-singular vectors of the jacobian
matrix of the hidden layers, which enables `60%` fooling UAPs from only `64` images!

### What it does
Presents an algorithm which allows generation of UAPs with as little as 64 images.
 
### How is it done
The goal is to push apart features from their original configuration. For that, we find the 
`epsilon` which maximizes the product `Jacobian * epsilon`. This `epsilon` is called the `(p,q)`
singular vector of the `jacobian`.

This is further executed using an iterative process which involves the `math-vec` function (must read!)
with the proposed power method.


### Chief Novelty
Showing that UAPs can be generated with as little as 64 images (though data-free approaches also exists.)

### Other Interesting Analysis

* Shows some positive correlation between the singular values found and the fooling rate (across networks, rather than across layers).

**Drawbacks**: No comparison to using simple gradient descent on the objective (instead of using `(p,q)`-singular value based update).


### Impressive Results



<p align="center">
  <img src="cvpr_2017/img/sv_uap_table.png" height="400" title="Defense Against UAP Table">
</p>
