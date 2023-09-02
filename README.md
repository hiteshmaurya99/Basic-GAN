# Basic GAN from scratch
This project is about understanding the fundamental idea behind GANs in its simplest form.
Dataset is Pokemon images form kaggle.
A usual i am using pytorch and its various libraries for image transformation and manipulation.
To load custom dataset i had to create a custom class inheriting the pytorch dataset and specipfy train and test transform to be performed.
[here is the sample of trianing data](url)

The core idea is we have two neural networks Generator and Discriminator, we fed the training image to the discriminator
which will try to learn its core representation pattern using Convolution2d layers and the Generator which accepts a random noise with the z latent dimension input channels(128, 256, 512 higher the better) and usamples the noisey input using convtranspose2d layers.
Discriminator outputs a probability of it being either fake or real(only zero or one).
Generator aims to output image close to input image to discriminator essentially fooling it.
Loss used her is simple binary crossentropy loss.

Training GANs are  tricky you dont want to get the discriminator become too powerful so after few epochs i turned off the discrimiantor training and trained only the Generator for some epochs, then both for 135 epochs on 22k images.
Smaller batch size gave better results and i ahave used pytoch's mixed precision for performance.
[output are nice considering the low epochs and simplicity of the model]

