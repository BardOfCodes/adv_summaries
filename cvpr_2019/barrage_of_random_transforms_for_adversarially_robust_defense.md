# Barrage of Random Transforms for Adversarially Robust Defense

#### Edward Raff, Jared Sylvester, Steven Forsyth and Mark McLean

### Abstract
Authors propose BaRT which combines multiple Individually weak defenses to build one strong defense. BaRT remains 
effective even after accounting for obfuscated gradients and achieves 24x improvement (?). 

### What it does
Use randomly selected transformations on the image while training as well as evaluation.
 
### How is it done
The authors propose applying selected transformations from 25 different transformation stochastically and in random 
sequence. As individually they provide weak defense, the authors posit that its the stochasticity of their combination 
that makes them effective. 

### Chief Novelty
Showing that Weak defenses can be combined stochastically to yield one strong defense mechanism.

### Other Interesting Analysis

* Use median instead of average gradient in EoT to deal with potential gradient obfuscation (as the mean might be 
ill-defined) (so may be the median?).

* The performance with 40 Iterations of EoT seems to be lesser than EoT at 10 Iterations. Slightly surprising.

* Show (In appendix) PGD with 520 steps, and also epsilon = 32 (IRL its perceptible after epsilon~10).

**Drawback** :  

* They use BPDA for all transformations. Is it necessary to train BPDA for all transformations? Why not use the actual function ?

* A study on the usefulness of the various transformations (in a Leave one out fasion) would have been nice! 

### Impressive Results


<p align="center">
  <img src="img/rand_t__results.png" height="400" title="Defense through Random Transformations Results">
</p>
