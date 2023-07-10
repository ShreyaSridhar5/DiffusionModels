# DiffusionModels
A project in which we repurposed code for diffusion models from [1] in order to generate images based on a new landscapes dataset. We also experimented with hyperparameters to measure their impact on performance. This project was submitted as the final project for the course _**CS449: Deep Learning**_ taught at _**Northwestern University (Evanston, Illinois, USA)**_ . 

For further detail on the goals of the project, and analysis of the results, see report.pdf.

## Important Files in this GitHub
1. run_model.py
 * Contains the script to load in all dependencies, import models, and begin training either the conditional or unconditional model.

2. ddpm.py
 * Contains the noising and denoising functions from [1] for the unconditional model. Also contains our code for saving and loading the model, and doing inference after the diffusion model has trained.

###### _Note: the code for the noising and denoising process of Diffusion is entirely from [1]. This is because our goal was not to start from the mathematical concepts of Diffusion from scratch, but to implement both a conditionally and unconditionally trained Diffusion Model. We focused on comparing the results from the 2 models and observing the results of changing hyperparameters for the noise schedule and UNet architecture._

3. ddpm_conditional.py
 * Contains the noising and denoising functions from [1] for the conditional model.
 * Contains our code for saving and loading the model, and doing inference after the Diffusion model has trained.
 * Contains our function for saving images for each class in a separate folder (for our GAN’s evaluation).
 
4. FID.ipynb
 * Contains the code that calculates the FID scores of images generated from both our conditional and unconditional diffusion models. This gives us an industry standard metric with which to judge the performance of our models.

5. GANClassifier.ipynb
 * Contains the code that trains and tests the classifier model from our 2nd desired goal, as well as further analysis on why we might be getting those particular results. It gives us another metric, besides FID score, with which to judge the performance of our conditional diffusion model.
 
6. utils.py
 * A file from [1] with functions that save images produced by the diffusion model and normalize input images from the training and testing dataset

7. modules
 * Includes the UNet architecture from [1].

8. download_images.ipynb
 * Unzipping our dataset into the Jupyter environment
 * Deleting directories once our model is done, to save credits for computation
 * Zipping up our results from the model
 * Folders with our result images have additionally been uploaded to GitHub.

## Works Cited
[1] https://github.com/tcapelle/Diffusion-Models-pytorch
