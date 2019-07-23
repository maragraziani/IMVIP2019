# Visualizing and interpreting feature reuse of pretrained CNNs for histopathology (submitted to IMVIP2019)
Mara Graziani, Vincent Andrearczyk and Henning Muller

paper still under review.

# How are the features learned by ImageNet pretrained CNNs reused in histopathology tasks? 

Transfer learning from networks pretrained on large scale datasets of natural images, such as ImageNet, is a diffuse practice in the medical imaging domain. The differences between medical images and ImageNet are, however, considerable. In histopathology images the variety of color, textures, backgrounds and objects is substantially shrunk to repetitive patterns (nuclei) as opposed to the wide diversity of natural images. 
Sources of variability are, for the most part, texture, shape irregularities and spatial arrangement of the cells.

The experiments in this paper aim at showing that feature reuse is mostly meaningful in the early layers of the network, which focus on identifying repetitive patterns and textures. 

# Experiments and Results



# Installation and Requirements 
The environment needed to run the experiments must include Tensorflow 1.8.0 and Keras 2.1.6.

See requirements.txt for the full list of python dependecies. 

These can be installed by running:
pip install -r requirements.txt


