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

- [D] Measuring whether all needed features by the model to make a prediction are selected by the explanation method = Comprehensiveness (AOPC) <a href="#deyoung">[4]</a> (Section 4.2)

- [E] Evaluating whether the identified salient features are enough to predict the same label as using the full text = Sufficiency (AOPC) <a href="#deyoung">[4]</a> (Section 4.2)

- [F] Log-odds = Averaging the difference of negative logarithmic probabilities on the predicted class over all of the test data before and after masking the top m% features with zero paddings <a href="#shrikumar">[5]</a>,<a href="#chen">[6]</a>

- [G] The degradation score to the trained model accuracy when higher-ranked features are recursively eliminated<a href="#nguyen">[7]</a>

- [H] Contrastive overlap score , Contrastive confidence score, Contrastive gain <a href="#babiker">[8]</a>

- [I] <a href="#kim">[9]</a> (Section 4.3)

- [J] <a href="#abid">[10]</a> (Section 4)

- [K] <a href="#yeh">[11]</a> (Sections 5.1, 5.2, 5.3)


## Problems to consider
- Differentiating between artifacts that stem from perturbing the data, a misbehaving model, and a misbehaving attribution method.
- The attributions can include undesirable artifacts of the adversarially constructed baseline. So we would like the baseline to convey a complete absence of signal, so that the features that are apparent from the attributions are properties only of the input, and not of the baseline. <a href="#Sundararajan17">[3]</a> (Section 5)




# References
<div class="csl-entry"> <a id="FESP"> [1] </a> Condevaux, Charles, Sebastien Harispe, et Stephane Mussard. « Fair and Eﬃcient Alternatives to Shapley-Based Attribution Methods », s. d., 16.
 </div>
 
<div class="csl-entry"> <a id="samek15"> [2] </a>  Samek, Wojciech, Alexander Binder, Gregoire Montavon, Sebastian Lapuschkin, et Klaus-Robert Muller. « Evaluating the Visualization of What a Deep Neural Network Has Learned ». IEEE Transactions on Neural Networks and Learning Systems 28, nᵒ 11 (novembre 2017): 2660‑73. https://doi.org/10.1109/TNNLS.2016.2599820.  </div>

<div class="csl-entry"> <a id="Sundararajan17"> [3] </a> Sundararajan, Mukund, Ankur Taly, et Qiqi Yan. « Axiomatic Attribution for Deep Networks ». arXiv, 12 juin 2017. https://doi.org/10.48550/arXiv.1703.01365. </div>

<div class="csl-entry"> <a id="deyoung"> [4] </a> DeYoung, Jay, Sarthak Jain, Nazneen Fatema Rajani, Eric Lehman, Caiming Xiong, Richard Socher, et Byron C. Wallace. « ERASER: A Benchmark to Evaluate Rationalized NLP Models ». arXiv, 24 avril 2020. https://doi.org/10.48550/arXiv.1911.03429. </div>

<div class="csl-entry"> <a id="shrikumar"> [5] </a> Shrikumar, Avanti, Peyton Greenside, et Anshul Kundaje. « Learning Important Features Through Propagating Activation Differences ». arXiv, 12 octobre 2019. https://doi.org/10.48550/arXiv.1704.02685. </div>

<div class="csl-entry"> <a id="chen"> [6] </a>Chen, Jianbo, Le Song, Martin J. Wainwright, et Michael I. Jordan. « L-Shapley and C-Shapley: Efficient Model Interpretation for Structured Data ». arXiv, 7 août 2018. https://doi.org/10.48550/arXiv.1808.02610. </div>

<div class="csl-entry"> <a id="nguyen"> [7] </a> Nguyen, Dong. « Comparing Automatic and Human Evaluation of Local Explanations for Text Classification ». In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), 1069‑78. New Orleans, Louisiana: Association for Computational Linguistics, 2018. https://doi.org/10.18653/v1/N18-1097. </div>

<div class="csl-entry"> <a id="babiker"> [8] </a> Babiker, Housam K B, Mi-Young Kim, et Randy Goebel. « Neural Networks with Feature Attribution and Contrastive Explanations », s. d., 16. </div>

<div class="csl-entry"> <a id="kim"> [9] </a>Kim, Been, Martin Wattenberg, Justin Gilmer, Carrie Cai, James Wexler, Fernanda Viegas, et Rory Sayres. « Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV) ». arXiv, 7 juin 2018. http://arxiv.org/abs/1711.11279.
</div>

<div class="csl-entry"> <a id="abid"> [10] </a>Abid, Abubakar, Mert Yuksekgonul, et James Zou. « Meaningfully Debugging Model Mistakes Using Conceptual Counterfactual Explanations ». In Proceedings of the 39th International Conference on Machine Learning, 66‑88. PMLR, 2022. https://proceedings.mlr.press/v162/abid22a.html.</div>

<div class="csl-entry"> <a id="yeh"> [11] </a>Yeh, Chih-Kuan, Been Kim, Sercan O. Arik, Chun-Liang Li, Tomas Pfister, et Pradeep Ravikumar. « On Completeness-aware Concept-Based Explanations in Deep Neural Networks ». arXiv, 7 février 2022. https://doi.org/10.48550/arXiv.1910.07969.</div>

<div class="csl-entry"> <a id=""> [] </a></div>


