# RnX_EVAL

## The following are references for evaluating the performance of explainibility methods

- [A] Mesuring the change in accuracy of prediction in model by ONLY keeping X% of top most important features obtained by the explain. method. <a href="#FESP">[1]</a>  (See section 4.1)

- [B] Selecting the top k pixels by attribution and randomly varying their intensities and then measuring the drop in score. <a href="#samek15">[2]</a> 

- [C] Considering images with human-drawn bounding boxes around objects, and computing the percentage of pixel attribution inside the box. <a href="#Sundararajan17">[3]</a> (Section 4)


## Problems to consider
- Differentiating between artifacts that stem from perturbing the data, a misbehaving model, and a misbehaving attribution method.





# References
<div class="csl-entry"> <a id="FESP"> [1] </a> Condevaux, Charles, Sebastien Harispe, et Stephane Mussard. « Fair and Eﬃcient Alternatives to Shapley-Based Attribution Methods », s. d., 16.
 </div>
 
 
<div class="csl-entry"> <a id="samek15"> [2] </a>  Samek, Wojciech, Alexander Binder, Gregoire Montavon, Sebastian Lapuschkin, et Klaus-Robert Muller. « Evaluating the Visualization of What a Deep Neural Network Has Learned ». IEEE Transactions on Neural Networks and Learning Systems 28, nᵒ 11 (novembre 2017): 2660‑73. https://doi.org/10.1109/TNNLS.2016.2599820.  </div>


<div class="csl-entry"> <a id="Sundararajan17"> [3] </a> Sundararajan, Mukund, Ankur Taly, et Qiqi Yan. « Axiomatic Attribution for Deep Networks ». arXiv, 12 juin 2017. https://doi.org/10.48550/arXiv.1703.01365. </div>


