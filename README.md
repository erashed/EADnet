# EADnet

Copyrights (c) 2021, Essam Rashed (essam (dot) rashed (at-sign) nitech.ac.jp), NITech, Nagoya, JP https://erashed.weebly.com

This code aims at forecasting of daily emergency ambulance dispatch (EAD) using meterological data and mobility estimate. 

This code is compatible with Mathematica 12.1 and beyond and tested over Windows 10, Ubuntu 16.04, and OSX 10.11.6. More details are in our paper mentioned below. If you are using this code, please refer to our paper.

-> Input data are in Microsoft Excel "*.xlsx" formats for easy use.

The Excel data formats is as follows (please create your own data file using the following structure):

Column A:> day

Column B:> month

Column C:> year

Column D:> mobility reduction estimate (normalized to scale 0-1)

Column E:> working day label (0: working day & 1: vacation/day off)

Column F:> daily maximum temprature

Column G:> daily average humidity

Column H:> total number of EAD

Column I:> number of EAD (children)

Column J:> number of EAD (adult)

Column K:> number of EAD (eldery)

Column L:> number of EAD (outdoor)

Column M:> number of EAD (indoor)

Note: I+J+K=L+M=H

Here, the original data used in the publication can not be shared for public use due to limitation of usage agreement.

-> To Run Select Evaluation -> Evaluate Notebook

-> If you are not familier with Mathematica Notebooks (*.nb), you can download free reader from here: http://www.wolfram.com/cdf-player/

"Preprocessing.nb"

This notebook will read the data and prepare data patchs. 

"SetParameters.nb"

This notebook can be used to set experiment parameters.

"LSTM_all.nb"

This notebook is the main code to conduct network training and validation.

"Archx.nb"

This notebook define network architecture


Reference

E. A. Rashed, S. Kodera, H. Shirakami, R. Kawaguchi, K. Watanabe, A. Hirata, "Knowledge discovery from emergency ambulance dispatch during COVID-19: A case study of Nagoya
City, Japan," Journal of Biomedical Informatics, 2021 (doi: https://doi.org/10.1016/j.jbi.2021.103743)
