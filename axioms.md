
<table>
  <tr>
    <th>Method</th>
    <th>Linearity<a href="#2">[2]</a></th>
    <th>Efficiency<a href="#2">[2]</a></th>
    <th>Symmetry<a href="#2">[2]</a></th>
    <th>Fair <br> treatment<a href="#2">[2]</a></th>
    <th>Sensitivity</th>
    <th>Implementation <br> Invariance <a href="#1">[1]</a></th>
    <th>Completeness<a href="#1">[1]</a></th>
  </tr>
  
  <tr>
    <td>DeConvNets</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">x</td>
    <td class="impl"></td>
    <td class="comp"></td>
  </tr>
  
  <tr>
    <td>Guided back-propagation</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">x</td>
    <td class="impl"></td>
  </tr>
  
  <tr>
    <td>DeepLift</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">o</td>
    <td class="impl">x</td>
  </tr>
  
  <tr>
    <td>LRP</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">o</td>
    <td class="impl">x</td>
  </tr>
  
  <tr>
    <td>IG</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">o</td>
    <td class="impl">o</td>
    <td class="comp">o</td>
  </tr>
  
  <tr>
    <td>Lime</td>
    <td class="lin"></td>
    <td class="eff"></td>
    <td class="symm"></td>
    <td class="fair"></td>
    <td class="sens">x<a href="#Sundararajan17">[1]</a></td>
    <td class="impl">o<a href="#Sundararajan17">[1]</a></td>
    <td class="comp"></td>
  </tr>
  
  
</table>
  

# Definitions:
### Linearity : 
- For all predictors f, g, an AM φ satisfies linearity if, φ(x, α1fi + α2gi) = α1φ(x, fi) + α2φ(x, gi), for all α1, α2 ∈ R and for all classes i ∈ C. <a href="#Condevaux22">[1]</a> (Section 3.1.)
### Efficiency
### Symmetry :
- For all inputs that have identical values for symmetric variables and baselines that have identical values for symmetric variables, the symmetric variables receive identical attributions. For instance, inputs x and y are symmetric w.r.t. F if and only if F (x, y) = F (y, x) for all values of x and y. <a href="#Sundararajan17">[1]</a> (Section 4.1.)
### Fair treatment
### Sensitivity :
- For every input and baseline that differ in one feature but have different predictions then the differing feature should be given a non-zero attribution.  <a href="#Sundararajan17">[1]</a> (Section 2.1.)
- If the function implemented by the deep network does not depend (mathematically) on some variable, then the attribution to that variable is always zero. <a href="#Sundararajan17">[1]</a> (Section 4.1.)
### Implementation Invariance
### Completeness
  
  

# References:
<div class="csl-entry"> <a id="Sundararajan17"> [1] </a> Sundararajan, Mukund, Ankur Taly, et Qiqi Yan. « Axiomatic Attribution for Deep Networks ». arXiv, 12 juin 2017. https://doi.org/10.48550/arXiv.1703.01365. </div>

<div class="csl-entry"> <a id="Condevaux22"> [2] </a> Condevaux, Charles, Sebastien Harispe, et Stephane Mussard. « Fair and Eﬃcient Alternatives to Shapley-Based Attribution Methods », s. d., 16. </div>
