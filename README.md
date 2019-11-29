# fw-adversarial-imagenet
Frank-Wolfe variant for adversarial attacks on Inception V3 model

* Paper 1: https://openreview.net/pdf?id=Hyewf3AqYX
* Paper 2: https://arxiv.org/pdf/1811.10828.pdf

## What is this notebook?

This notebook implements a few Frank-Wolfe variants which can be used for adversarial attacks on images.

Attacks are performed against Inception V3 model, on images from Imagenet Validation dataset.
I present some experiments with different hyperparameters and results of comparisons.

Theoretical background can be found in Paper 1. In addition to the white and black box implementations from the paper above, I have implemented a modified Frank-Wolfe algorithm with momentum, from Paper 2.

The main difference between two papers and the original Frank Wolfe method is as follows:
* Paper 1 (algorithms White box and Black box) calls the linear minimization oracle over a more relaxed constraint set
* Paper 2 implements the momentum term which nudges the gradient in the direction of the previous step

The notebook is intended as an educational tool. As such, explainability is favoured over performance (hence the use of the notebook). 
While effort was made to use efficient Python, the efficiency of code can be improved vastly by the use of sessions, GPU processing, and running through Terminal.
