# Visualizing and interpreting feature reuse of pretrained CNNs for histopathology (IMVIP2019)
Mara Graziani, Vincent Andrearczyk and Henning Muller

All the channel visualizations and class activations maps can be 
inspected in the folder interpretability_results/.

Particularly, the visualization patchworks are useful to inspect all the images at once.  

# How are the features learned by ImageNet pretrained CNNs reused in histopathology tasks? 

Transfer learning from networks pretrained on large scale datasets of natural images, such as ImageNet, is a diffuse practice in the medical imaging domain. The differences between medical images and ImageNet are, however, considerable. In histopathology images the variety of color, textures, backgrounds and objects is substantially shrunk to repetitive patterns (nuclei) as opposed to the wide diversity of natural images. 
Sources of variability are, for the most part, texture, shape irregularities and spatial arrangement of the cells.

The experiments in this paper aim at showing that feature reuse is mostly meaningful in the early layers of the network, which focus on identifying repetitive patterns and textures. 

# Experiments and Results
The code for running the experiments is grouped in the following notebooks:

- visualize_channels_CNN.ipynb: imports the network graph and weights after finetuning and uses the lucid4keras[1] wrapper to generate the visualizations. Results in interpretability_results/inceptionv3_finetuned. 
This code was also applied to visualize the channel activations of InceptionV3 pretrained on ImageNet. See details in the notebook.

<p align="center">
    <img src="interpretability_results/patchwork_finetuned_iv3.png" width=700px>
</p>


- lucid_iv3.ipynb: loads the lucid[2] toolbox and the InceptionV3 from the modelzoo to visualize intermediate channel activations of the pretrained network (results in interpretability_results/lucid_inceptionv3). The same results can be obtained by using the ImageNet pretrained parameters in visualize_channels_CNN (see results in interpretability_results/inceptionv3) 

<p align="center">
    <img src="interpretability_results/patchwork_lucid_iv3.png" width=700px>
</p>


- gradcam_plus.ipynb: visualizes the gradCAM and gradCAM++ heatmaps overlayed on the input images. Results in interpretability_results/gradcam and interpretability_results/gradcamplus

<p align="center">
    <img src="interpretability_results/patchwork_gradcamplus.png" width=700px>
</p>


- RCVs_analysis.ipynb: code for the last experiment on the regression of concept measures of texture in the network layers. Results in interpretability_results/rcvs

# Datasets and Models

To get the same dataset and model parameters used for the experiments contact me at mara.graziani@hevs.ch.

# Installation and Requirements 
The environment needed to run the experiments must include Tensorflow 1.8.0 and Keras 2.1.6.

See requirements.txt for the full list of python dependecies. 

These can be installed by running:
pip install -r requirements.txt


