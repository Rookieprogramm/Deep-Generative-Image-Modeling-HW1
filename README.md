# Deep-Generative-Image-Modeling-HW1
- Comparison of AE and VAE

## Project Description
A variational autoencoder is used to learn recoverable data in an unsupervised manner. In this topic, you
need to design the autoencoder and variational autoencoder by PyTorch, train on eye datasets, and analyze
two models by quantitative and qualitative comparisons, respectively.

### Data
There are two classes in the given dataset (data.npy), containing female eyes (0) and male eyes (1). The total
number of data is 1476 and the shape of each image is (50, 50, 3). You have to read and merge them. The
Google Drive download link of the given dataset is shown below:
[https://drive.google.com/file/d/171seEF6LXJeuzOIHWhl2BGpMFR22NVl1/view](https://drive.google.com/file/d/171seEF6LXJeuzOIHWhl2BGpMFR22NVl1/view)
<figure>
<img src="https://github.com/user-attachments/assets/eb891c45-08fe-4ce0-b28f-af4f6bf446e5" style="width:100%">
<figcaption align = "center"> Figure 1. Examples of the given eye dataset </figcaption>
</figure>

### Structure of Dataset 
eye.zip<br>
&emsp;| --- data.npy<br> 
&emsp;| --- label.npy <be> 

## Implementation 
Please employ the autoencoder and variational autoencoder to reconstruct the image. 

1. Design your own PyTorch Dataset Class to load the data and labels, then merge them into a Class. You 
can read the images with any package, e.g., PyTorch, PIL, cv2, etc. 
2. Design your CNN-based autoencoder and variational autoencoder model. 
3. Train the designed AE and VAE in Step 2 on all 1476 images with the dataset constructed in Step 1. Save the models after finishing the training process. 
4. Evaluate the average PSNR and SSIM scores of the trained AE and VAE models in Step 3 on all 1476 images. Note that you should load the trained models before starting evaluations. The **average PSNR should surpass 25** and the **average SSIM should surpass 0.7** for both AE and VAE models. Please use **skimage** to conduct the evaluations. 
5. Save 20 reconstruction results for both AE and VAE models in Step 3 respectively. You can save them as jpg or png files. For fairness, we specified the image ID as [91-95, 481-485, 936-940, 1446-1450]. Note that the image index range is defined as 1-1476. 
6. Please add the “same” Gaussian noise into the trained VAE and AE models in Step 3, and repeat Step 5. The demonstration of adding noise to VAE is shown in Fig. 2
<figure>
<img src="https://github.com/user-attachments/assets/815e86f6-fec8-4cc0-8762-c8e8c29d1859" style="width:100%">
<figcaption align = "center"> Fig. 2 The diagram of adding the Gaussian noise into a latent vector on VAE  </figcaption>
</figure>
