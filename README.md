# Reference-based-SR

In this project, we intend to conduct an in-depth study in the field of reference-based-SR. Ref SR refers to supplementing the details of the input low resolution (LR) image by introducing rich textures of the high resolution (HR) image. In the initial stage of my research, I intend to study existing papers. My supervisors recommended the following papers to me, and I intend to conduct in-depth analysis and study on them.
## Papers and codes:
paper name|Innovation method|Code|Source
----|-----|------|-------
Robust Reference-based Super-Resolution via C2-Matching [paper](https://arxiv.org/abs/2106.01863)|Contrastive Correspondence Network + Teacher-Student Correlation Distillation: cross transformation, cross resolution|[Code](https://github.com/yumingj/C2-Matching)|CVPR, 2021
Feature Representation Matters: End-to-End Learning for Reference-based Image Super-resolution [paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123490222.pdf)|E2ENT: transfer the relevant textures from reference image to the output SR image|Not found|ECCV, 2020
Towards Content-Independent Multi-Reference Super-Resolution: Adaptive Pattern Matching and Feature Aggregation [paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123700052.pdf)|RP, LFE|Not found|ECCV, 2020
CrossNet: An End-to-end Reference-based Super Resolution Network using Cross-scale Warping [paper](https://arxiv.org/pdf/1807.10547.pdf)|image encoders + cross-scale warping layer + fusion decoders. End-to-end, large-scale.|[Code](https://github.com/htzheng/ECCV2018_CrossNet_RefSR)|ECCV, 2018
Variational AutoEncoder for Reference based Image Super-Resolution [paper](https://arxiv.org/pdf/2106.04090.pdf)|RefVAE: VGG + CVAE + image decoder. Any image can be used as a reference and multiple SR images can be generated.|[Code](https://github.com/Holmes-Alan/RefVAE)|CVPR, 2021
MASA-SR: Matching Acceleration and Spatial Adaptation for Reference-Based Image Super-Resolution [paper](https://arxiv.org/pdf/2106.02299.pdf)|MASA-SR: Match & Extration Mpdule + Spatial Adaptation Module. To boost the rubustness of the network when dealing with Ref images with different distributions.|[Code](https://github.com/dvlab-research/MASA-SR)|CVPR, 2021
Robust Reference-based Super-Resolution with Similarity-Aware Deformable Convolution [paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Shim_Robust_Reference-Based_Super-Resolution_With_Similarity-Aware_Deformable_Convolution_CVPR_2020_paper.pdf)|Three layers of deformable convolution, Dynamic Offset Estimator|Not found|CVPR, 2020

## Datasets
dataset|number|type|introduction|download
---|----|-----|------|-------
CUFED|1883 albums, 30-100 images in each album|Raw images|Each album describes an event. The album's event types come from 23 common events in everyday life, such as weddings and trips.|[download](https://drive.google.com/file/d/0BxBaqbArti0NMlF4aG05c3h2NU0/view)
Urban100|100|Raw images|The content is photos of the city, generally used to test performance. LR/HR image pairs can be obtained by bicubic interpolation.|[download](https://www.kaggle.com/msahebi/super-resolution)
DIV2K|1000|2K raw images|800 images for training, 100 images for validation, 100 images for testing|[download](https://drive.google.com/drive/folders/1B-uaxvV9qeuQ-t7MFiN1oEdA6dKnj2vW)
W2S|44,000 real fluorescence microscopy images, resulting in a total of 360 sets of images|RGB images|The noise-free LR images are the average of 400 raw images, and the HR images are obtained using structured-illumination microscopy (SIM).|[download](https://zenodo.org/record/3895807#.YJOu0egzabg)
PIPAL|250 reference images, 29000 distortion images|Raw images|40 distortion types, including the output of GAN-based algorithms|[train data download](https://drive.google.com/drive/folders/1G4fLeDcq6uQQmYdkjYUHhzyel4Pz81p-) [validation data download](https://drive.google.com/drive/folders/1w0wFYHj8iQ8FgA9-YaKZLq7HAtykckXn)
DPED|22,000|Raw images|LR images: photos taken by different smartphones. Reference: photos taken by Canon DSLR|[download](https://drive.google.com/file/d/0BwOLOmqkYj-jeUJwQjRNUFkzOTA/view?resourcekey=0-C5SGM--H8oLNY5TR61tRlA)
RealSR|559 scenes (459 scenes for training & 100 scenes for testing)|Raw images|LR-HR image pairs are obtained by adjusting the focal length of the digital camera|[download](https://drive.google.com/file/d/1Iqx3AbUlLjR_JglsQIq9y9BEcrNLcOCU/view)
Flickr2K|2650|Raw images|People, animals, landscapes|[download](https://drive.google.com/drive/folders/1B-uaxvV9qeuQ-t7MFiN1oEdA6dKnj2vW)
Vimeo-90K|89,800|videos|It is a data set constructed by Tianfan Xue et al. for video hypersegmentation, video noise reduction, video artifact removal and video frame insertion|[download](http://toflow.csail.mit.edu/)
## knowledge distillation methods
SRKD:  
teacher network: 3 parts.  
1)convolution layer + ReLU  
2)10 * residual blocks  
3)deconvolutional layer  
student network: 3 parts.  
1)convolution layer + ReLU  
2)3 * depthwise separable block  
3)deconvolutional layer  
  
  asfa

