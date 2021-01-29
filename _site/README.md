# Rethinking Road Surface 3D Reconstruction and Pothole Detection: From Perspective Transformation to Disparity Map Segmentation

This repository provides the data used in our recent publication "[Rethinking Road Surface 3D Reconstruction and Pothole Detection: From Perspective Transformation to Disparity Map Segmentation](https://arxiv.org/pdf/2012.10802.pdf)". 

**A story behind this work:**

- When working on this project, I was a third-year Ph.D. student at the University of Bristol. 

- When submitting this paper, I was a fresh postdoc at HKUST. 

- When this work was finally accepted, I have been working at UCSD for almost a year, and my postdoc career is nearly coming to an end...

We experienced a very annoying review process for this paper. It was originally submitted for peer-review on **Apr. 11, 2019**. We got the initial feedback on **Jul. 28, 2019**, and resubmitted our first revision on **Aug. 22, 2019**. However, nothing was back to us until **Jul. 09, 2020** (after DOZENS of emails from us enquiring about the reviewer's feedback). We submitted the second revision on **Aug. 06, 2020**, and FINALLY got accepted on **Jan. 01, 2021**. So, it was reviewed for **21 months**. In my opinion, this work is already out-of-date when it was published. Anyway, I am going to provide you with the data we used in this work. 

## 1. Road Pothole 3D Geometry Reconstruction Dataset: 

In our [previous work](https://www.ruirangerfan.com/pdf/tip2018_fan.pdf), the accuracy of the reconstructed 3D road surface was evaluated using three sample models printed with a MakerBot Replicator 2 Desktop 3D Printer. This is an indirect way! Therefore, in this work, we evaluated the accuracy of the reconstructed road potholes in a straightforward way. 

We first poured enough gypsum plaster into a pothole and dug the gypsum mold out, when it became dry and hardened. Then, we used a [BQ Ciclop 3D laser scanner](https://www.amazon.com/Ciclop-Scanner-Kit-Advanced-Laser/dp/B014G8GMEO) (assembled and calibrated by ourselves). We provide the materials regarding the assembly and calibration of a BQ Ciclop 3D laser scanner in [laser_scanner](./laser_scanner) folder. An example of our used laser scanner and the obtained gypsum mold is shown below:

<p align="center">
<img src='./figs/laser_scanner.jpg' width=400px>
</p>

An example of the 3D pothole model reconstructed using the laser scanner is shown below:

<p align="center">
<img src='./figs/3d_model.gif' width=500px>
</p>

Then, we use the iterative closest point (ICP) algorithm to register the road pothole point clouds A and B (see below), which are acquired using laser scanning and stereo vision technologies, respectively. 

<p align="center">
<img src='./figs/registration.png' width=600px>
</p>

Our experimental results indicate that the road pothole 3D geometry reconstructed using stereo vision technology achieved an accuracy of 2.23 mm. The stereo road images pairs and their ground-truth road pothole 3D geometry models are provided in [dataset](./dataset) folder. 


## 2. Road Pothole Detection Dataset

The pothole detection dataset can be download from this [repository](https://github.com/ruirangerfan/stereo_pothole_datasets). You can run our demo code to see the visualization of different types of road data. Some examples of the road pothole detection results are shown below:

<p align="center">
<img src='./figs/pothole_detection_results.png' width=900px>
</p>

where (a) left road images, (b) transformed disparity images (obtained using our previously published [disparity transformation algorithm](https://github.com/ruirangerfan/unsupervised_disparity_map_segmentation)), (c)-(f) pothole detection results achieved using [1], [2], [3] and our method, respectively. The quantitative results are also shown below:

<p align="center">
<img src='./figs/results.png' width=900px>
</p>

## 3. Citation
Please cite the following papers when using our road data:





## References
[1]