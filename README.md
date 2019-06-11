# Meta-Signer

Meta-Signer is a machine learning aggregated approach for feature evaluation of metagenomic datasets. Random forest, support vector machines, LASSO, multi-layer neural networks, and our novel PopPhy-CNN machine learning frameworks are used to train and evaluate features in a cross-validated fashion. Features are then aggregated across models and partitions into a single ranked list of the top *k* features.

## Execution:

We provide a python environment which can be imported using the [Conda](https://www.anaconda.com/distribution/) python package manager.

Deep learning models are built using [Tensorflow](https://www.tensorflow.org/). Meta-Signer was designed using **Tensorflow v1.12.0**.

To fully utilize GPUs for faster training of the deep learning models, users will need to be sure that both [CUDA](https://developer.nvidia.com/cuda-toolkit-archive) and [cuDNN](https://developer.nvidia.com/cudnn) are properly installed.

Other dependencies should be downloaded upon importing the provided environment.

### Clone Repository
```bash
git clone https://github.com/YDaiLab/Meta-Signer.git
cd Meta-Signer
```
### Import Conda Environment

```bash
conda env create -f meta-signer.yml
source activate meta-signer
``` 
### Set configuration settings

Meta-Signer offers a flexible framework which can be customized in the configuration file.

**If you want to run Meta-Signer without deep learning models and without Tensorflow, make sure to set the 'Train' parameter to False in config.py.**

### Run the Meta-Signer pipeline:

```bash
cd src
python meta-signer.py
``` 

