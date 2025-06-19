# AlliGator-Plugin-IntensityOverThresholdMask

AlliGator Python plugin to create a mask of ROIs defined by pixels with 
peak intensity over a set threshold. This plugin essentially reproduces the 
function of the right-click Source Image menu item <code>ROIs:Create ROI(s) 
from Pixels with Peak above Min</code>.

1. To run the plugin, first load a FLI dataset.
An example from the paper "In vitro and in vivo phasor analysis of stoichiometry 
and pharmacokinetics using short lifetime near‐infrared dyes and time‐gated 
imaging", Journal of Biophotonics 12 (3), e201800185, 
[doi:10.1002/jbio.201800185](https://doi.org/10.1002/jbio.201800185) by SJ Chen, 
N Sinsuebphon, A Rudkouskaya, M Barroso, X Intes, X Michalet is provided in the 
*data* folder.

2. To determine an appropriate threshold value, one approach consists in looking 
at the brightest gate in the dataset (in which the peak value of most pixels 
will most likely be) and use the image histogram *Min* cursor to highlight 
pixels with intensity lower than *Min*. Choose a *Min* color (at the bottom of 
the Source Image color scale) that is easily dsitinguishable from the rest of 
the palette (green in the example below). An appropriate threshold will leave a 
few regions of the image untouched.

![Threshold determination](/images/Threshold-determination.png)

3. Select the plugin function item (<code>Analysis:FLI Dataset:FLI Dataset 
Plugin Example:Peak Intensity Above Threshold Mask</code>) in the menu bar and 
enter the value estimated from the previous step in the *Value* column and 
press *Enter*.

![Enter threshold](/images/Enter-threshold.png)

4. The result of the plugin action (a Mask image) should appear as shown below. 
Check the Notebook for additional information, or in case of an error, for 
indication of what may have gone wrong.

![Mask image output](/images/Mask-image-output.png)

5. The Mask Image is automatically converted into ROIs, which can be selected 
in the **Source Image ROI Manager** window (<code>Windows:Source Image ROI 
Manager</code>). The figure below shows the original dataset with all the 
detected ROIs (obtained using the <code>ROIs:Show All ROIs</code> Source Image 
right-click menu item).