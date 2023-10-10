# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().
### Step2
Convert the saved BGR image to RGB using cvtColor().
### Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.
### Step4
Apply the filters using cv2.filter2D() for each respective filters.
### Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().
## Program:
### Developed By   :SARGURU.K
### Register Number:212222230134

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("di.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/120
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("on")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("di.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/12
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Weighted Averaging Filter Image")
plt.axis("on")
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("di.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Filter Image")
plt.axis("on")
```

iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("di.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Filter Image")
plt.axis("on")
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("di.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernel Filtered Image")
plt.axis("on")
```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("di.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title(" Laplacian operator Filtered Image")
plt.axis("on")
```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/5f34a07a-171d-4163-8b66-27af88f499f4)


ii) Using Weighted Averaging Filter
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/1fa235d4-0e72-45ff-8b13-aecda58d4f5c)


iii) Using Gaussian Filter
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/ffc43e40-24a9-437a-9deb-217b20aad393)


iv) Using Median Filter
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/90544a02-d934-4e3f-94f1-7a7add2d0b3f)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/10020b2e-ad06-49cc-9ed7-76bbbef24352)
ii) Using Laplacian Operator
![download](https://github.com/BaskaranV15/IMPLEMENTATION-OF-FILTERSS/assets/118703522/d0dd0721-9346-4e20-aee4-5c91f79c8d77)
## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
