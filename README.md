# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.

## Program:
### Developed By   : RAJA R
### Register Number: 212222100041
</br>

### 1. Smoothing Filters

#### i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("galaxy.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
#### ii) Using Weighted Averaging Filter
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()







```
#### iii) Using Gaussian Filter
```Python


gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()






```

#### iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()







```

### 2. Sharpening Filters
#### i) Using Laplacian Kernal
```Python


kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()






```
#### ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()






```

## OUTPUT:
### 1. Smoothing Filters


#### i) Using Averaging Filter
![Screenshot 2024-03-19 201609](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/28ecbc8e-1294-46e7-b00c-cfb1f687899b)


#### ii) Using Weighted Averaging Filter
![Screenshot 2024-03-19 201638](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/edab4133-2be2-4984-9cf1-30511703afd1)


#### iii) Using Gaussian Filter

![Screenshot 2024-03-19 201712](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/74398e81-3b06-427d-afaa-fc3f887f21b5)

#### iv) Using Median Filter
![Screenshot 2024-03-19 201740](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/8b140a9a-2048-4946-a96a-cd6549ae6b8f)


### 2. Sharpening Filters


#### i) Using Laplacian Kernal
![Screenshot 2024-03-19 201807](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/7cd25756-41a8-457f-9c28-adb6094bf7ae)


#### ii) Using Laplacian Operator
![Screenshot 2024-03-19 201836](https://github.com/Raja8334/Implementation-of-filter/assets/120719634/7949c5f6-c685-4ff6-8553-7eabf63ab39f)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
