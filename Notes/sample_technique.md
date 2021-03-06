# Sampling Technique

## 1. Direct Method

The sample is generated by

$$X = F_x^{-1}(U), U \sim Uniform. $$



## 2. Accept/Reject Algorithm

Let $X\sim f_x(x)$ and $V \sim f_V(v)$, where $f_V$ and $f_X$ have common support with 

$$M = sup_y \frac{f_X(x)}{f_V(x)} < \infty$$.

The algorithm generating r.v. $X \sim f_X$ is:

- Step 1: Generate $U \sim U(0,1)$, $V \sim f_V$, independent
- Step 2:  If $U < \frac{1}{M}\frac{f_{X}(V)}{f_V(V)}$,  set $X=V$; otherwise, return to step 1.

### 2.1 proof

Using conditional distribution to show the $Y$ we g get has the same cdf with target distribution

### 2.2 Comment

- The step 2 illustrates how likely the sample is draw from target density.
- The number of trials needed to generate one $X$ is a $Geometric(\frac{1}{M})$ r.v., and M is the expected number of trials. So a better $V$ is a r.v. whose distribution achieves a smaller $M$.
- The $V$ should have heavier tails than the density $X$, to get a good representation of target r.v.
- When the target density has heavy tail, and it is difficult to get candidate density that will result in a finite values of $M$, Accept/Reject Algorithm will no longer apply. 



## 3. Metropolis Algorithm

To be filled after finishing *Pattern Recognition and Machine Learning*.

## 4. Gibbs Algorithm

To be filled after finishing *Pattern Recognition and Machine Learning*.

