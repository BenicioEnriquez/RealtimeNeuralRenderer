# Real-time Neural Renderer
![Banner Logo](https://polybiustech.github.io/NeuralRenderer/static/images/teaser.png)

Latent diffusion models have high speed image synthesis capabilities that can used for manipulating existing images and synthetic 3D geometry with ease, having the potential to greatly increase the perceived realism with minimal effort.

## The Idea
Neural rendering is a technology that could greatly revolutionize the field of computer graphics. By removing the dependency upon high resolution textures and complicated global illumination methods to generate photorealistic images, we can substantially increase the capabilities of prodecural generation algorithms, since a much lower level of detail is necessary. In place of these, we can use generative AI models to fill in the gaps so that the frames retain a high level of intricacy, and allow us to switch themes, styles, and settings instantaneously. In this project, I will explore the usage of Latent Consistency Models as a method of realtime neural rendering, in conjunction with StreamDiffusion, ControlNet and TemporalConsistency models.

## Demo


## Implementation
This project repository is structured around the fantastic [StreamDiffusion](https://github.com/cumulo-autumn/StreamDiffusion). StreamDiffusion builds upon the existing work of Latent Consistency Models (LCM), which explore a method of distilling Stable Diffusion generative image models allowing them to produce coherent results in a fraction of the time (~50 steps -> ~5 steps). StreamDiffusion improves upon LCMs by introducing a batch diffusion pipeline, trading memory for speed. In addition, the authors present a novel residual classifier-free guidance (RCFG) algorithm that signifcantly outperforms the existing classifier-free guidance by up to 2.05x. By utilizing StreamDiffusion and finetuning the hyperparameters for quality and speed, we were able to acheive coherent visual results at an average frame rate of 13.9 fps on an RTX 3060, with minimal latency. 
