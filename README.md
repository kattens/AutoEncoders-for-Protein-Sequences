# AutoEncoders-for-Protein-Sequences

This repository contains the implementation of Variational Autoencoders (VAEs) and Normal Autoencoders (AEs) for protein sequences. Autoencoders are unsupervised learning models that can learn a compressed representation of the input data. In the context of protein sequences, autoencoders can be used to capture meaningful features and patterns in the sequences, which can be useful for tasks such as protein function prediction, sequence generation, and protein structure prediction.

## Introduction

Autoencoders are neural network models consisting of an encoder and a decoder. The encoder compresses the input data into a lower-dimensional latent space representation, while the decoder aims to reconstruct the original input data from the latent representation. Variational Autoencoders (VAEs) introduce a probabilistic approach to autoencoders, which allows for sampling from the learned latent space.

This repository provides the implementation of both VAEs and AEs for protein sequences. By training these models on a dataset of protein sequences, you can learn compressed representations that capture relevant information about the sequences.

## Model Architecture

The autoencoder models used in this repository consist of a recurrent neural network (RNN) encoder and decoder. The encoder processes the input sequence and produces a fixed-length vector as the latent representation. The decoder takes the latent vector and generates a reconstructed sequence.

For VAEs, the latent space is modeled as a Gaussian distribution with mean and variance parameters. The encoder outputs the parameters of the distribution, and sampling is performed by drawing samples from the distribution during training and generation.

## Training

During training, the autoencoder models aim to minimize the reconstruction loss, which measures the difference between the input sequence and the reconstructed sequence. In the case of VAEs, an additional term is added to the loss function to encourage the latent space to follow the desired distribution.

Training progress and model performance are logged and saved in the output directory specified during training. The logs include information such as loss values, model checkpoints, and visualizations of the reconstructed sequences.

## Evaluation

To evaluate a trained autoencoder model, the script computes various metrics such as reconstruction loss and generates visualizations of the reconstructed sequences. The evaluation results are displayed in the console.

### References

Here are some references that you may find useful for understanding autoencoders and their applications in protein sequence analysis:

    Kingma, D. P., & Welling, M. (2014). Auto-Encoding Variational Bayes. arXiv preprint arXiv:1312.6114.
    Hinton, G. E., & Salakhutdinov, R. R. (2006). Reducing the dimensionality of data with neural networks. Science, 313(5786), 504-507.
    Angermueller, C., Pärnamaa, T., Parts, L., & Stegle, O. (2016). Deep learning for computational biology. Molecular systems biology, 12(7), 878.
