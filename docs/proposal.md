# Project Proposal

## 1. Motivation & Objective

The motivation of this project came from a scenario when a surveillance system is both resource and bandwidth limited. The captured images maybe low in quality and there is not enough connectivity to send the low-quality image to a server. We are trying to create a mechanism that would be capable of reconstructing the low-quality image from a fraction of its pixel information (limited bandwidth connectivity) and enhancing the reconstructed low-quality image to a higher resolution.

## 2. State of the Art & Its Limitations

Currently, there are separate solutions to problems of low bandwidth connectivity and low-quality data acquisition. Compressive sensing is used to reconstruct the full image from only a fraction of the original pixel size. SRCNN (Super Resolution Convolutional Neural Networks) are used to enhance low-quality/blurry images. However, in a situation where both the camera quality and bandwidth connectivity is compromised, there does not exist a single solution. Using a two-step process of Compressive sensing and SRCNN might be a plausible method however, both Compressive sensing and Deep Neural Networks are known to be computationally expensive. 

## 3. Novelty & Rationale

A single mechanism (using deep neural networks) capable of both data reconstruction and enhancement is a good applicable solution. Such an algorithm of image-enhancing from limited pixel information is to a large extent, something not yet explored.

## 4. Potential Impact

If successful, such a model will have many uses throughout the different industries for data reconstruction and enhancement. In many rural areas technology is bandwidth limited and camera quality is poor. As a result, transmitted data is not usable. Our algorithm can take such input and provide analyzable results.

## 5. Challenges

Designing an architecture which chooses pixels to imitate compressive sensing (for reconstruction), Training a neural net is extremely resource-intensive in the system, Choosing the hyperparameters for superresolution.

## 6. Requirements for Success

Familiarity with SRCNNs and Compressive sensing, Programming skills in Python, A desktop/Computer with good enough specification (GPU) to train a Neural network, Image processing skills.

## 7. Metrics of Success

We will measure the Structural Similarity Index (SSIM) of the reference image (an original image that was downsized to create the test data image) to the result to measure the reconstruction and enhancement quality.

## 8. Execution Plan

We will first decide what size of the image we would want to work with then find datasets from ImageNet. We will downscale the image and send a fraction of the downscaled image and use Bicubic interpolation and our own Super Resolution Deep net to enhance it. Then we will measure the Structural Similarity Index (SSIM) netween the original image and output image to measure the reconstruction and enhancement quality. We both will be working on finding datasets, building and training our CNN, and the evaluation process. Arunachalam with previous experience with deep nets will help Shyandeep catch up with concepts and we will execute the plan as a team.

## 9. Related Work

### 9.a. Papers

ESRGAN: Enhanced Super-Resolution Generative Adversarial Networks [1]

Neural Networks for Compressed Sensing Based on Information Geometry [2]

Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network [3]

Neural signal compressive sensing [4]

Stable signal recovery from incomplete and inaccurate measurements [5]

These papers gave us an idea of how to use deep nets for image enhancement as well as reconstruction. We borrowed a lot from these papers and are trying to implement a model which aims to achieve a similar goal.

### 9.b. Datasets

ImageNet [6]

### 9.c. Software

Python Libraries: OpenCV[7], NumPy[8], Matplotlib[9], Torch[10], Torchvision[11]

## 10. References

[1] Wang X. et al. (2019) ESRGAN: Enhanced Super-Resolution Generative Adversarial Networks. In: Leal-Taixé L., Roth S. (eds) Computer Vision – ECCV 2018 Workshops. ECCV 2018. Lecture Notes in Computer Science, vol 11133. Springer, Cham. https://doi.org/10.1007/978-3-030-11021-5_5

[2] Wang, M., Xiao, CB., Ning, ZH. et al. Neural Networks for Compressed Sensing Based on Information Geometry. Circuits Syst Signal Process 38, 569–589 (2019). https://doi.org/10.1007/s00034-018-0869-6

[3] C. Ledig et al., "Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network," 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2017, pp. 105-114, doi: 10.1109/CVPR.2017.19.

[4] Denise Fonseca Resende, Mahdi Khosravy, Henrique L. M. Monteiro, Neeraj Gupta, Nilesh Patel, Carlos A. Duque, "Neural signal compressive sensing", Chapter 11, Compressive Sensing in Healthcare, 2020, Pages 201-221, https://doi.org/10.1016/B978-0-12-821247-9.00016-0.

[5] Emmanuel J. Candès, Justin K. Romberg, Terence Tao, "Stable signal recovery from incomplete and inaccurate measurements", Communication on pure and applied mathematics, Vol- 59, Issue- 8, https://doi.org/10.1002/cpa.20124

[6] ImageNet (https://www.image-net.org/)

[7] OpenCV (https://opencv.org/)

[8] NumPy (https://numpy.org/)

[9] Matplotlib (https://matplotlib.org/)

[10] Torch (https://torch.io/)

[11] Torchvision (https://pytorch.org/vision/stable/index.html)
