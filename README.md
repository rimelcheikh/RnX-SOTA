# RnX - State of the art of explanation methods for deep neural networks

## Problem formalization

![image](https://user-images.githubusercontent.com/81907010/181770346-ea579d57-50d3-49c8-862e-43bef09675d6.png)

Reverse engineering approach for explaining deep neural networks : <br>
the learned black box predictor is queried with a test dataset D={X,Y} to produce an oracle &#374;, which associate to each sample x∈X, a label that is not real but assigned by the black box

## Methods in terms of : data type, NN type, explanator, problem and reproducibility

- Data types : Images (IMG), Text (TXT), Tabular (TAB), Anything (ANY) 
- Black Boxes : Deep neural networks (DNN), Convolutional neural networks (CNN), Recurrent neural networks (RNN), Agnostic (AGN)
- Explanator : Feature importance (FI), Saliency map (SM)
- Problem : Outcome explanation (OUT), Model explanation (MOD)

<table>
  <tr>
    <th>Name</th>
    <th>Data type</th>
    <th>Black Box</th>
    <th>Explanator</th>
    <th>Problem</th>
    <th>Code</th>
    <th>BB Model</th>
    <th>Dataset</th>
    <th>Examples</th>
  </tr>
  
  <tr>
    <td>GRAD-CAM <a href="#grad-cam">[1]</a> </td>
    <td>IMG</td>
    <td>CNN</td>
    <td>SM</td>
    <td>OUT</td>
    <td><a href="https://github.com/ramprs/grad-cam/">&#x2713; </a> </td>
    <td><a href="https://github.com/karpathy/neuraltalk2">Neuraltalk2</a> </td>
    <td><a href="https://cocodataset.org/#download">COCO</a> </td>
    <td>&#x2713;</td>
  </tr>
  
  <tr>
    <td>LIME <a href="#lime">[2]</a> </td>
    <td>ANY</td>
    <td>AGN</td>
    <td>FI</td>
    <td>OUT</td>
    <td><a href="https://github.com/marcotcr/lime">&#x2713; </a> </td>
    <td>&#x2713; (many)</td>
    <td>&#x2713; (many)</td>
    <td>&#x2713;</td>
  </tr>
  
  <tr>
    <td>DnCShap <a href="#dncshap">[3]</a> </td>
    <td>IMG</td>
    <td>CNN</td>
    <td>FI</td>
    <td>OUT</td>
    <td><a href="https://github.com/MIntelligence-Group/InterpretableFER">&#x2713; </a> </td>
    <td><a href="https://github.com/MIntelligence-Group/InterpretableFER">FER </a> </td>
    <td><a href="https://zenodo.org/record/3451524#.YuPbpnZBy3A"> JAFFE </a> </td>
    <td>&#x2713;</td>
  </tr>
  

  
  
</table>


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
    <td>GRAD-CAM <a href="#grad-cam">[1]</a> <br> DnCShap <a href="#dncshap">[1]</a> </td>
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


## Review Papers
<div class="csl-entry"> Guidotti, R., Monreale, A., Ruggieri, S., Turini, F., Giannotti, F., &#38; Pedreschi, D. (2018). A Survey of Methods for Explaining Black Box Models. <i>ACM Computing Surveys (CSUR)</i>, <i>51</i>(5). https://doi.org/10.1145/3236009</div>

<div class="csl-entry"> Samek, W., Montavon, G., Lapuschkin, S., Anders, C. J., &#38; Müller, K. R. (2021). Explaining Deep Neural Networks and Beyond: A Review of Methods and Applications. <i>Proceedings of the IEEE</i>, <i>109</i>(3), 247–278. https://doi.org/10.1109/JPROC.2021.3060483</div>


## References:
<div class="csl-entry"> <a id="grad-cam"> [1] </a> Selvaraju, R. R., Cogswell, M., Das, A., Vedantam, R., Parikh, D., &#38; Batra, D. (n.d.). <i>Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization</i>. https://github.com/</div>

<div class="csl-entry"> <a id="lime"> [2] </a> Ribeiro, M. T., Singh, S., &#38; Guestrin, C. (2016). “Why Should I Trust You?”: Explaining the Predictions of Any Classifier. <i>NAACL-HLT 2016 - 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Proceedings of the Demonstrations Session</i>, 97–101. https://doi.org/10.48550/arxiv.1602.04938</div>

<div class="csl-entry"><a id="dncshap"> [3] </a> Malik, S., Kumar, P., &#38; Raman, B. (2021). Towards Interpretable Facial Emotion Recognition <i>Proceedings of the Twelfth Indian Conference on Computer Vision, Graphics and Image Processing</i>. https://doi.org/10.1145/3490035.3490271</div>
