# RnX - State of the art of explanation methods for deep neural networks

## Problem formalization

![image](https://user-images.githubusercontent.com/81907010/181770346-ea579d57-50d3-49c8-862e-43bef09675d6.png)

Reverse engineering approach for explaining deep neural networks : <br>
the learned black box predictor is queried with a test dataset D={X,Y} to produce an oracle &#374;, which associate to each sample x∈X, a label that is not real but assigned by the black box

## Methods in terms of : data type, NN type, explanator, problem and reproducibility

- Data types : Images (IMG), Text (TXT), Tabular (TAB), Anything (ANY) 
- Black Boxes : Deep neural networks (DNN), Convolutional neural networks (CNN), Recurrent neural networks (RNN), Agnostic (AGN)
- Explanator : Feature importance (FI), Saliency map (SM), Marginal Contribution (MC), Neural Circuit (NC)
- Family : Interpretable Local Surrogates (ILS), Occlusion Analysis (OA), Layerwise Relevance Propagation (LRP), Attribution methods(AM), Concept-Based (CB)
- Problem : Outcome explanation (OUT), Model explanation (MOD)

<table>
  <tr>
    <th>Name</th>
    <th>Data type</th>
    <th>Black Box</th>
    <th>Explanator</th>
    <th>Family</th>
    <th>Problem</th>
    <th>Code</th>
    <th>BB Model</th>
    <th>Dataset</th>
    <th>Examples</th>
    <th>Evaluation</th>
    <th>Axiomatic</th>
  </tr>
  
  <tr>
    <td>GRAD-CAM (2017)<a href="#grad-cam">[1]</a> </td>
    <td>IMG</td>
    <td>CNN</td>
    <td>SM</td>
    <td>AM</td>
    <td>OUT</td>
    <td><a href="https://github.com/ramprs/grad-cam/">&#x2713; </a> </td>
    <td><a href="https://github.com/karpathy/neuraltalk2">Neuraltalk2</a> </td>
    <td><a href="https://cocodataset.org/#download">COCO</a> </td>
    <td>&#x2713;</td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>LIME (2016)<a href="#lime">[2]</a> </td>
    <td>ANY</td>
    <td>AGN</td>
    <td>FI</td>
    <td>ILS</td>
    <td>OUT</td>
    <td><a href="https://github.com/marcotcr/lime">&#x2713; </a> </td>
    <td>&#x2713; (many)</td>
    <td>&#x2713; (many)</td>
    <td>&#x2713;</td>
    <td class="eval"></td>
    <td class="axioms"></td>
  </tr>
  
  <tr>
    <td class="name">ES + FESP (2022)<a href="#fesp">[3]</a> </td>
    <td class="dt">IMG TXT</td>
    <td class="bb">DNN</td>
    <td class="expl">MC</td>
    <td class="fam">AM</td>
    <td class="prob">OUT (MOD)</td>
    <td class="code"><a href="https://github.com/ccdv-ai/fesp_es">&#x2713; </a> </td>
    <td class="bbmod"><a href="https://keras.io/api/applications/vgg/">imgs</a>
                  <a href="https://huggingface.co/textattack/roberta-base-imdb">txt</a></td>
    <td class="ds"><a href="https://www.robots.ox.ac.uk/~vgg/data/pets/">imgs</a>
                  <a href="https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews">txt</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/RnX_eval.md">[A]</a></td>
    <td class="axioms">&#x2713;</td>
  </tr>
  
  <tr>
    <td class="name">IG (2017)<a href="#ig">[4]</a> </td>
    <td class="dt">ANY</td>
    <td class="bb">DNN</td>
    <td class="expl">FI</td>
    <td class="fam">AM</td>
    <td class="prob">OUT</td>
    <td class="code"><a href="https://github.com/ankurtaly/Integrated-Gradients">&#x2713; </a></td>
    <td class="bbmod"><a href="https://pytorch.org/hub/pytorch_vision_googlenet/">GoogleNet</a><br>   
                        <a href="https://github.com/yoonkim/CNN_sentence">CNNSC</a><br>   
                        GNMT<br>W2N2</td>
    <td class="ds"><a href="https://www.image-net.org/">ImageNet</a> <br>
                        <a href="https://github.com/ppasupat/WikiTableQuestions">WikiTableQuestions</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval">&#x2715;</td>
    <td class="axioms">&#x2713;</td>
  </tr>
  
  <tr>
    <td class="name">Bisturi (2022)<a href="#bisturi">[5]</a> </td>
    <td class="dt">IMG</td>
    <td class="bb">CNN</td>
    <td class="expl">NC</td>
    <td class="fam">CB</td>
    <td class="prob">MOD</td>
    <td class="code"><a href="https://github.com/rmassidda/bisturi">&#x2713;</a> </td>
    <td class="bbmod">AlexNet ResNet DenseNet </td>
    <td class="ds"><a href="https://github.com/CSAILVision/places365">Places-365</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval">&#x2715;</td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  <tr>
    <td class="name">ContInt<a href="#contr">[6]</a> </td>
    <td class="dt">TXT</td>
    <td class="bb">DNN</td>
    <td class="expl">FI</td>
    <td class="fam">AM</td>
    <td class="prob">MOD</td>
    <td class="code">&#x2715;</td>
    <td class="bbmod"><a href="https://github.com/tensorflow/tensor2tensor">multi-head</a></td>
    <td class="ds"><a href="https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews">IMDB</a><br> 
                  <a href="https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset">AG News</a><br> 
                  <a href="https://www.yelp.com/dataset">YELP</a></td>
    <td class="ex">&#x2713;</td>
    <td class="eval"><a href="https://github.com/rimelcheikh/RnX-SOTA/blob/main/RnX_eval.md">[D,E,F,G,H]</a></td>
    <td class="axioms">&#x2715;</td>
  </tr>
  
  <tr>
    <td class="name"><a href="#">[]</a> </td>
    <td class="dt"></td>
    <td class="bb"></td>
    <td class="expl"></td>
    <td class="fam"></td>
    <td class="prob"></td>
    <td class="code"><a href=""></a> </td>
    <td class="bbmod"><a href=""></a></td>
    <td class="ds"><a href=""></a></td>
    <td class="ex"></td>
    <td class="eval"></td>
    <td class="axioms">&#x2713;</td>
  </tr>
 
  

  
  
</table>

<!--- 
## Methods in terms of : problem, data type, NN

### Outcome explanation
<table>
  <tr>
    <th></th>
    <th>IMG</th>
    <th>TAB</th>
    <th>TXT</th>
    <th>ANY</th>
  </tr>
  
  <tr>
    <td>DNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>CNN</td>
    <td>GRAD-CAM <a href="#grad-cam">[1]</a></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>RNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>NN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>AGN</td>
    <td></td>
    <td></td>
    <td></td>
    <td>LIME <a href="#lime">[2] </a></td>
  </tr>
</table>

### Model explanation
<table>
  <tr>
    <th></th>
    <th>IMG</th>
    <th>TAB</th>
    <th>TXT</th>
    <th>ANY</th>
  </tr>
  
  <tr>
    <td>DNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>CNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>RNN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>NN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  
  <tr>
    <td>AGN</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
-->

## Review Papers
<div class="csl-entry"> Guidotti, R., Monreale, A., Ruggieri, S., Turini, F., Giannotti, F., &#38; Pedreschi, D. (2018). A Survey of Methods for Explaining Black Box Models. <i>ACM Computing Surveys (CSUR)</i>, <i>51</i>(5). https://doi.org/10.1145/3236009</div>

<div class="csl-entry"> Samek, W., Montavon, G., Lapuschkin, S., Anders, C. J., &#38; Müller, K. R. (2021). Explaining Deep Neural Networks and Beyond: A Review of Methods and Applications. <i>Proceedings of the IEEE</i>, <i>109</i>(3), 247–278. https://doi.org/10.1109/JPROC.2021.3060483</div>


## References:
<div class="csl-entry"> <a id="grad-cam"> [1] </a> Selvaraju, R. R., Cogswell, M., Das, A., Vedantam, R., Parikh, D., &#38; Batra, D. (n.d.). <i>Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization</i>. https://openaccess.thecvf.com/content_iccv_2017/html/Selvaraju_Grad-CAM_Visual_Explanations_ICCV_2017_paper.html </div>

<div class="csl-entry"> <a id="lime"> [2] </a> Ribeiro, M. T., Singh, S., &#38; Guestrin, C. (2016). “Why Should I Trust You?”: Explaining the Predictions of Any Classifier. <i>NAACL-HLT 2016 - 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Proceedings of the Demonstrations Session</i>, 97–101. https://doi.org/10.48550/arxiv.1602.04938</div>

<div class="csl-entry"> <a id="fesp"> [3] </a> Condevaux, Charles, Sebastien Harispe, et Stephane Mussard. (2022). Fair and Eﬃcient Alternatives to Shapley-Based Attribution Methods <i>ECMLPKDD 2022-The European Conference on Machine Learning and Principles and Practice of Knowledge Discovery in Databases.</i>, https://2022.ecmlpkdd.org/wp-content/uploads/2022/09/sub_477.pdf </div>

<div class="csl-entry"> <a id="ig"> [4] </a> Sundararajan, Mukund, Ankur Taly, et Qiqi Yan. « Axiomatic Attribution for Deep Networks ». arXiv, 12 juin 2017. https://doi.org/10.48550/arXiv.1703.01365. </div>

<div class="csl-entry"> <a id="bisturi"> [5] </a> Massidda, Riccardo, and Davide Bacciu. "Knowledge-Driven Interpretation of Convolutional Neural Networks." </div>

<div class="csl-entry"> <a id="contr"> [6] </a> Babiker, Housam K B, Mi-Young Kim, et Randy Goebel. « Neural Networks with Feature Attribution and Contrastive Explanations », s. d., 16. </div>
