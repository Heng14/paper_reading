### Nerf:Neural Radiance Fields

[**project**](https://www.matthewtancik.com/nerf)|[**paper**](https://arxiv.org/abs/2003.08934)[|**code**](https://github.com/bmild/nerf)

#### **Overview**

Using network to learn a 5D vector-valued function. Input 3D location x = (x; y; z) and 2D viewing direction (θ; Φ). Output color c = (r; g; b) and volume density (α). Then use volume rendering to generate a particular viewpoint image.

Steps:

1. March camera rays through the scene to generate a sampled set of 3D points
2. Use those points and their corresponding 2D viewing directions as input to the neural network to produce an output set of colors and densities
3. use classical volume rendering techniques to accumulate those colors and densities into a 2D image

![](img/nerf_pipeline.jpg)

#### **Technique**

1. Discrete set of samples to represent continuous volume rendering equation.
2. **Positional encoding**

​		Similar idea as Transformer.

2. **Hierarchical volume sampling**

​		Optimize two networks: one “coarse” and one “fine”.

#### **Note**

1.The Optimization here is happening for a deep fully connected multi-layer perceptron without using any convolutional layers. 

2.Gradient descent is used to optimize this model by minimizing the error between each observed image and the corresponding views rendered from the representation.

3.Nerf works well on images of static subjects captured under controlled settings.

4.Incapable of modeling many ubiquitous, real-world phenomena in uncontrolled images, such as variable illumination or transient occluders.
