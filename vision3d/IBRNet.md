### IBRNet: Learning Multi-View Image-Based Rendering

CVPR 2021

[**project**](https://ibrnet.github.io/)|[**paper**](https://arxiv.org/abs/2102.13090)|[**code**](https://github.com/googleinterns/IBRNet)

#### **Overview**

*We present a method that synthesizes novel views of complex scenes by interpolating a sparse set of nearby views.*

<img src="img/ibrnet.png" style="zoom:30%;" />

#### **Technique**

1. **View selection and feature extraction**

   Synthesize the novel target view by interpolating nearby source views.

   Use a shared U-Net based convolutional neural network to extract dense features

   

2. **Volume density prediction**

    Multi-view feature aggregation. 

   Ray transformer.



#### **Note**

1. Trained on large amounts of data, this method is able to generalize well to novel scenes.

