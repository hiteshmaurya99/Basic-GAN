# Basic GAN from scratch
This project is about understanding the fundamental idea behind GANs in its simplest form.
Dataset is Pokemon images form kaggle.
A usual i am using pytorch and its various libraries for image transformation and manipulation.
To load custom dataset i had to create a custom class inheriting the pytorch dataset and specipfy train and test transform to be performed.
[here is the sample of trianing data](url)

The data core idea is we have two neural networks Generator and Discriminator, we fed the training image to the discriminator
which will try to learn its core representation pattern using Convolution2d layers and then 
