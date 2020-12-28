# Single-Image-Colorization-and-Super-Resolution

This project aims at colorizing grey images and increase their quality. This is my effort along with my teamates (Mohamed Mahfouz and Omar Shaheen), and was done as a part of PMDL project at AUC.

The Super Resolution Part was done using Two networks (Modified EDSR and DQE). This is a variation of the EDSR Model (https://arxiv.org/abs/1707.02921) and to the best of our knowlege was not implemented elsewhere. 
The idea is to have two networks one to upscale the image by 2x and the other is to make the image more natural. This architecture performs better than the EDSR- one example of the descent performance can be seen below. 
<img src="/imgs/2.jpg">
more examples can be found in the notebook (EDSR-DQE) while the regular EDSR can be found in EDSR_base notebook. This architecture was trained 16k 128 by 128 by 3 images, and were
fed to the model using TF Dataset Generator. The number of trainable parameters was about 6M parameters.

For the Colorization part, a deep CNN was used with about 24M trainable parameters with the last layer predicting the AB channels of the LAB color scale. Then the AB predicted channels
are joined with the L channel giving the colorized image. A test of the whole model can be found in notebook (EDSR-DQE). 

The Super resolution part works pretty well, but the colorization still needs more work. 

The trained model of the Super resolution can be found here: https://drive.google.com/drive/folders/18qxMDF06z5dUNc_rb-J5nFqXzM3CNkCB?usp=sharing

For more information, plase check the paper and the poster of the project. Shall you have any questions, email them.
