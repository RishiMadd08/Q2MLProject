Variational Autoencoders (VAEs) are a popular
method for learning compressed representations of images, but
they have a major limitation: they assume the latent space
follows a simple Gaussian distribution. This ”one size fits all”
assumption doesn’t work well for datasets like MNIST, where
each digit should ideally form its own cluster. In this project, we
implement a hierarchical model that combines three techniques:
a convolutional VAE to compress images, a normalizing flow
to make the latent distribution more flexible, and a Gaussian
Mixture Model to capture multiple modes. We trained this
model on MNIST using a stage-wise approach where each
component is optimized separately. Our experiments compare
this against simpler baselines to see if the extra complexity
actually helps. Results show that our model improves classifier-
based accuracy substantially (from 0.820 to 0.943, a relative
increase of approximately 14.9% over the baseline), raises mean
classifier confidence from 0.909 to 0.972, reduces KL divergence
of generated class frequencies vs. uniform from 0.0445 to 0.0086
(an ≈80.7% reduction), and yields a mean component purity of
0.853 for the fitted mixture components.

Note: The creation date for code is changed because we had to make a new Github account
