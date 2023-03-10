# Description

A 3D neural network based algorithm for volumetric segmentation of 3D medical images.

# Model Overview

This model is trained using the SOTA res-UNet with deep supervision 

## Training configuration

The training was performed with at least 16GB-memory GPUs.

## commands example

Execute model training:

```
CUDA_VISIBLE_DEVICES=0 python scripts/train.py run --config_file=configs/hyper_parameters.yaml
```

Execute multi-GPU model training (recommended):

```
torchrun --nproc_per_node=gpu scripts/train.py run --config_file=configs/hyper_parameters.yaml
```

Execute validation:

```
python scripts/validate.py run --config_file=configs/hyper_parameters.yaml
```

Execute inference:

```
python scripts/infer.py run --config_file=configs/hyper_parameters.yaml
```

# Disclaimer

This is an example, not to be used for diagnostic purposes.

# References

[1] Myronenko, A., 2018, September. 3D MRI brain tumor segmentation using autoencoder regularization. In International MICCAI Brainlesion Workshop (pp. 311-320). Springer, Cham.
