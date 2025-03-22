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
### Developed By   :MANOJ M
### Register Number:212223230122
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("color_image.jpeg")
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
ii) Using Weighted Averaging Filter
```Python


kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()


```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
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
ii) Using Laplacian Operator
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

![Screenshot 2025-03-22 173448](https://github.com/user-attachments/assets/5179ac38-f86c-463f-a08c-1a0db4ff09e1)

ii)Using Weighted Averaging Filter

![Screenshot 2025-03-22 173457](https://github.com/user-attachments/assets/eadfdfe2-b88e-4081-99cf-94ac95da87be)


iii)Using Gaussian Filter

![Screenshot 2025-03-22 173505](https://github.com/user-attachments/assets/1056791f-6bbc-4beb-8da9-6bb4d5065e53)


iv) Using Median Filter

![Screenshot 2025-03-22 173517](https://github.com/user-attachments/assets/094899e5-ea57-493a-ac75-d4bcb3798498)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![Screenshot 2025-03-22 173530](https://github.com/user-attachments/assets/e078d578-9333-4b5c-8e9a-4a260c00baac)

ii) Using Laplacian Operator

![Screenshot 2025-03-22 173542](https://github.com/user-attachments/assets/eb42508a-d5eb-4081-986b-494840c0c077)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
