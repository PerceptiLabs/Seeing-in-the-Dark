<p align="center">
  <a href="https://www.perceptilabs.com">
  <img src="./pl_logo.png">
  </a>
</p>

# Seeing in the Dark
This example PerceptiLabs model, shows how a special type of [convolutional neural network (CNN)](https://en.wikipedia.org/wiki/Convolutional_neural_network) called a [U-Net](https://en.wikipedia.org/wiki/U-Net), can be used to enhance dark photos. 

The concept behind this approach is based on that described in *Learning to See in the Dark (SID)*, a scholarly article published on [https://arxiv.org/abs/1805.01934](https://arxiv.org/abs/1805.01934) that demonstrates how machine learning (ML) can be used in place of traditional digital image processing techniques, to enhance very dark images. 

The resources provided in this GitHub repo, supplement our [Using a U-Net to Enhance Dark Photos](https://www.perceptilabs.com/docs/u-net_usecase) documentation topic.

Happy hacking!

# Structure
This repo has the following structure:
* **/Data**: contains pre-processed versions of the raw data/reference image pairs to use for training that originated as raw camera data files in the SID project. The pairs of images are stored in the following subdirectories. Note that each pair uses the same filenames for the raw data and reference images:
  * **/Data/short_cropped**: contains the raw, dark camera sensor data images that have been preprocessed, cropped, and spatially reduced to a resolution of 512x512x4 in .tiff format.
  * **/Data/long_cropped**: contains the corresponding reference images with the ideal lighting that have been preprocessed and cropped to a resolution of 1024x1024x3 (sRGB) in .tiff format.
* **/SID_Model**: contains the PerceptiLabs model file (model.json).

# Installation

**Note**: you must be running PerceptiLabs 0.10.0 or higher to load this model.

Follow the steps below to load the sample model in PerceptiLabs:

1. Clone or download the sample model from GitHub.
2. On the ModelHub screen, import the sample model into PerceptiLabs. When prompted for the model's folder, navigate to and select the location of the **model.json** file.
3. Open the topmost **Data** component in the model workspace and set its folder to the **long_cropped** directory.
Open the second **Data** component in the model workspace and set its folder to the **short_cropped** directory.

# Community

Got questions, feedback, or want to join a community of machine learning practitioners working with exciting tools and projects? Check out our [Community page](https://www.perceptilabs.com/community)!


