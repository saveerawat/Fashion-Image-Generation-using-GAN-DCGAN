# Fashion-Image-Generation-using-GAN-DCGAN
**1. Project Description**

This project explores Generative Adversarial Networks (GANs) and Deep Convolutional GANs (DCGANs) to generate synthetic fashion images (e.g., dresses) using a custom dataset.
<br>It includes two Jupyter Notebooks:<br>
1️. GAN_fashion.ipynb – Fully connected (MLP-based) GAN<br>
2️. DCGAN_fashion.ipynb – Convolution-based GAN (DCGAN) for improved image quality

Both models are trained on 64×64×3 dress images, normalized and processed from a custom dataset.

**2. Dataset**

The dataset consists of dress images stored in Google Drive. (https://drive.google.com/drive/u/2/folders/1wE3nptThJyMPKj_R8Cs5S_pjyeAxtN4Y)

All images were resized to 64×64×3.<br>
Train set: ~15,379 images<br>
Test set: ~154 images<br>
Images were normalized to the range [-1, 1] for GAN training.

**3. Model Architecture**

Generator:
Takes a 100-dimensional noise vector, Uses Dense + LeakyReLU layers, Outputs a 64×64×3 synthetic fashion image, Learns to create realistic dress images

Discriminator:
Takes a 64×64×3 image (real or fake), Uses Dense + LeakyReLU + Dropout layers, Outputs a probability (real vs fake), Learns to detect fake images

GAN (Generator + Discriminator):
Generator tries to fool the discriminator, Discriminator tries to correctly classify images, Trained adversarially to improve both networks

DCGAN Improvement:
Uses Conv2D/Conv2DTranspose instead of Dense layers, Learns spatial patterns (edges, textures, clothing shapes), Produces clearer and more detailed images, Overcomes limitations of normal GAN (blurry/incomplete patterns)
