# RnX_EVAL

## Categories of existing evaluation techniques for XAI methods (Wilming et al. 2022):
- Evaluating the sensitivity or robustness of explanations to model modifications and input perturbations ( = sanity checks <=> correctness of explanations) :
    - Similar inputs should lead to similar explanations (Alvarez-Melis & Jaakkola 2018)
    - Detection of inadequate explanations (Ancona et al. 2018)
    - The identified features of trained models are akin to the ones identified by randomized models (Adebayo et al. 2018) (Hooker et al. 2019)
    - Identified features often represent low-level properties of the inputs (Adebayo et al. 2018) (Sixt et al. 2020)
- Using interdisciplinary and human-centered techniques to evaluate explanations (Doshi-Velez and Kim 2017):
    - Measure the extent to which the use of model ‘explanations’ can help a human to accomplish a task or to predict a model’s behavior (Baehrens et  al. 2010) (Poursabzi-Sangdeh et  al. 2021) (Lage et  al. 2018) (Schmidt and Biessmann 2019)
    - Define ground-truth explanations directly through human expert judgement (Park et al. 2018)
- Establishing a controlled setting by leveraging a-priori knowledge about relevant features (Ground-truth-centered evaluations):
    - Use of synthetic data to obtain qualitative ‘explanations’, which were then evaluated by humans (Kim et al. 2018)
    - Derived quantitative statements from synthetic data (Yang and Kim 2019)
    - Defining the importance of features through a generative process (Ismail et al. 2019) (Tjoa and Guan 2020) (Wilming et al. 2022)

## The following are references for evaluating the performance of explainibility methods

- [A] Mesuring the change in accuracy of prediction in model by ONLY keeping X% of top most important features obtained by the explain. method. <a href="#FESP">[1]</a>  (See section 4.1)

- [B] Selecting the top k pixels by attribution and randomly varying their intensities and then measuring the drop in score. <a href="#samek15">[2]</a> 

- [C] Considering images with human-drawn bounding boxes around objects, and computing the percentage of pixel attribution inside the box. <a href="#Sundararajan17">[3]</a> (Section 4)


## Problems to consider
- Differentiating between artifacts that stem from perturbing the data, a misbehaving model, and a misbehaving attribution method.
- The attributions can include undesirable artifacts of the adversarially constructed baseline. So we would like the baseline to convey a complete absence of signal, so that the features that are apparent from the attributions are properties only of the input, and not of the baseline. <a href="#Sundararajan17">[3]</a> (Section 5)




# References
<div class="csl-entry"> <a id="FESP"> [1] </a> Condevaux, Charles, Sebastien Harispe, et Stephane Mussard. « Fair and Eﬃcient Alternatives to Shapley-Based Attribution Methods », s. d., 16.
 </div>
 
 
<div class="csl-entry"> <a id="samek15"> [2] </a>  Samek, Wojciech, Alexander Binder, Gregoire Montavon, Sebastian Lapuschkin, et Klaus-Robert Muller. « Evaluating the Visualization of What a Deep Neural Network Has Learned ». IEEE Transactions on Neural Networks and Learning Systems 28, nᵒ 11 (novembre 2017): 2660‑73. https://doi.org/10.1109/TNNLS.2016.2599820.  </div>


<div class="csl-entry"> <a id="Sundararajan17"> [3] </a> Sundararajan, Mukund, Ankur Taly, et Qiqi Yan. « Axiomatic Attribution for Deep Networks ». arXiv, 12 juin 2017. https://doi.org/10.48550/arXiv.1703.01365. </div>


