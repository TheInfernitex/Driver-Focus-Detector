<div class="cell markdown">
## Driver-Focus-Detector
</div>

<div class="cell markdown">
### Problem Description
</div>

<div class="cell markdown">
Given driver photos, each taken in a car
with a driver doing something in the car (texting, eating, talking on
the phone, makeup, reaching behind, etc). Your goal is to predict the
likelihood of what the driver is doing in each picture.

The 10 classes to predict are as follows, <br> <br> <table> <tr> <td>
<li>c0: safe driving</li> <br> <li>c1: texting - right</li> <br> <li>c2:
talking on the phone - right</li> <br> <li>c3: texting - left</li> <br>
<li>c4: talking on the phone - left</li> <br> <li>c5: operating the
radio</li> <br> <li>c6: drinking</li> <br> <li>c7: reaching behind</li>
<br> <li>c8: hair and makeup</li> <br> <li>c9: talking to passenger</li>
</td> <td> 
</td> </tr>
</table>
</div>

<div class="cell markdown">
### Summary of Results
</div>

<div class="cell markdown">
Using a 50-layer Residual Network (with the following parameters) the
following scores (losses) were obtained. <table> <li>10 Epochs</li>
<li>32 Batch Size</li> <li>Adam Optimizer</li> <li>Glorot Uniform
Initializer</li> <tr> <td> **Training Loss** </td> <td> 0.93 </td> </tr>
<tr> <td> **Validation Loss** </td> <td> 3.79 </td> </tr> <tr> <td>
**Holdout Loss** </td> <td> 2.64 </td> </tr> </table>

**Why the high losses? Simply put - we don't have enough resources to
quickly iterate / hyper-parameter tune the model\!** If more resources
were available (RAM, CPU speed), we could hyper-parameter tune over grid
searches and combat high bias / high variance, which this model
currently suffers. [This is how you'd fix high bias/variance.](#improve)
</div>
