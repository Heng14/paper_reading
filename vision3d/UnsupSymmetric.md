### Unsupervised Learning of Probably Symmetric Deformable 3D Objects from Images in the Wild

CVPR 2020

[**project**](https://elliottwu.com/projects/unsup3d/)|[**paper**](https://arxiv.org/abs/1911.11130)|[**code**](https://github.com/elliottwu/unsup3d)

#### **Overview**

*We propose a method to learn 3D deformable object cate- gories from raw single-view images, without external super- vision.*

<img src="img/unsupsym1.png" style="zoom:50%;" />

#### **Technique**

1. **Photo-geometric autoencoding**

   Image I -> *depthmap* d, *albedo image* a, *light direction* l, *viewpoint* w 

   The image I is reconstructed from the four factors in two steps, *lighting* Λ and *reprojection* Π

   <img src="img/unsupsym2.png" style="zoom:50%;" />

2. **Probably symmetric objects**

    Flip the map d and a. Obtain a second reconstruction I from the

   flipped depth and albedo:

   <img src="img/unsupsym3.png" style="zoom:50%;" />
   
   then we have loss:
   
   <img src="img/unsupsym4.png" style="zoom:50%;" />
   
   <img src="img/unsupsym5.png" style="zoom:50%;" />

3. **Perceptual loss**

   <img src="img/unsupsym6.png" style="zoom:50%;" />


#### **Note**



