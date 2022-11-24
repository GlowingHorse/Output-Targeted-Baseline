# Aumann-Shapley Baseline Calculation in Convolutional Neural Networks

For the paper 'Output-targeted baseline for neuron attribution calculation'

Quickstart
===
## Installation
0. It is safer to create a virtual environment before installing libraries in *requirements.txt*.
1. Install necessary libraries listed in *requirements.txt*.

## Usage
1. Run *gen_AS_baseline.py* to generate Aumann-Shapley attribution baseline.
2. Run *gen_attr_results.py* to calculate neuron attributions.

## For mask perturbation
- The settings of `transforms` in *gen_attr_results.py* and fractal noise pyramid intensity (`image_sample`) in *./utils/render_baseline.py* can be finetuned according to network strucutre for better results.  
- Although the current objective function `loss` in *./utils/render_baseline.py* can produce the best results, we still keep some other tested losses in comments, hoping to give you some new ideas. All these losses can be easily reused in similar visualization tasks.

## Others
- Some other attribution methods are provided in *gen_attr_results.py*, but generally, we find Aumann-Shapley method is a good to calculate neuron attributions.  
The attribution calculation framework is implemented with reference to [**DeepExplain**](https://github.com/marcoancona/DeepExplain).  
- When you try different networks that are provided in [**TensorFlow-Slim**](https://github.com/tensorflow/models/tree/master/research/slim#pre-trained-models), the transform methods and some random image preconditioning settings should be changed accordingly.
