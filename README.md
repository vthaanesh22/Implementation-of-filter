# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1

 Import the required libraries.

## Step2

 
Convert the image from BGR to RGB.

## Step3

Apply the required filters for the image separately.

## Step4

Plot the original and filtered image by using matplotlib.pyplot.

## Step5

End the program.



## Program:
### Developed By   : THAANESH.V
### Register Number: 212223230228


## 1. Smoothing Filters

### i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("paris.jpg")
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


### ii) Using Weighted Averaging Filter

```
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






### iii) Using Gaussian Filter

```
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


### iv) Using Median Filter

```
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

## 2. Sharpening Filters

###  i) Using Laplacian Kernal
```

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
### ii) Using Laplacian Operator

```
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

## i) Using Averaging Filter

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/f85ed3bf-b748-4ce9-a313-d9f339bbe353)



## ii) Using Weighted Averaging Filter

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/fccd1b9a-b261-4807-9d3b-e71d82de155f)



## iii) Using Gaussian Filter

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/91c6c7af-0fec-4969-936e-daee395ed6c4)





## iv) Using Median Filter

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/02d979a3-a348-460c-b1dd-6b5c3d625c83)


### 2. Sharpening Filters


## i) Using Laplacian Kernal

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/932b0f1b-0642-4714-9d7e-d374734f2d87)





## ii) Using Laplacian Operator

![image](https://github.com/22009150/Implementation-of-filter/assets/118708624/8569350d-2c2c-4d6d-bc42-7ce860db630a)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
