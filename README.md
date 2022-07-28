# RnX - State of the art of explanation methods for neural networks

## Review Papers
<div class="csl-entry"> Guidotti, R., Monreale, A., Ruggieri, S., Turini, F., Giannotti, F., &#38; Pedreschi, D. (2018). A Survey of Methods for Explaining Black Box Models. <i>ACM Computing Surveys (CSUR)</i>, <i>51</i>(5). https://doi.org/10.1145/3236009</div>

<div class="csl-entry"> Samek, W., Montavon, G., Lapuschkin, S., Anders, C. J., &#38; Müller, K. R. (2021). Explaining Deep Neural Networks and Beyond: A Review of Methods and Applications. <i>Proceedings of the IEEE</i>, <i>109</i>(3), 247–278. https://doi.org/10.1109/JPROC.2021.3060483</div>

## Methods in terms of : data type, NN type, explanator, problem and reproducibility

- Data types : Images (IMG), text (TXT), tabular (TAB)
- Black Boxes : Deep neural networks (DNN), Convolutional neural networks (CNN), Recurrent neural networks (RNN), 
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
    <td><a href="https://github.com/ramprs/grad-cam/">&#x2713;</a> </td>
    <td></td>
    <td></td>
    <td></td>
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
    <td>GRAD-CAM <a href="#grad-cam">[1]</a> </td>
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





## References:
<div class="csl-entry"> <a id="grad-cam"> [1] </a> Selvaraju, R. R., Cogswell, M., Das, A., Vedantam, R., Parikh, D., &#38; Batra, D. (n.d.). <i>Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization</i>. https://github.com/</div>

