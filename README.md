# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Read and show the image
### Step2
Apply the filtering technique that we want to perform
### Step3
Show the filtered image

## Program:
### Developed By   : Nithishkumar P
### Register Number:  212221230070
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel1 = np.ones((11,11),np.float32)/121
box_filter = cv2.filter2D(original_image,-1,kernel1)
cv2.imshow('box_filter',box_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
ii) Using Weighted Averaging Filter
```Python

#ii) Using Weighted Averaging Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
cv2.imshow('weighted_filter',weighted_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
iii) Using Gaussian Filter
```Python
#iii) Using Gaussian Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0,
sigmaY=0)
cv2.imshow('gaussian_filter',gaussian_blur)
cv2.waitKey(0)
cv2.destroyAllWindows()





```

iv) Using Median Filter
```Python

#iv) Using Median Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
median = cv2.medianBlur(src=original_image,ksize = 11)
cv2.imshow('median_filter',median)
cv2.waitKey(0)
cv2.destroyAllWindows()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


#i) Using Laplacian Kernal
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
cv2.imshow('laplacian_kernel',laplacian_kernel)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
ii) Using Laplacian Operator
```Python
#ii) Using Laplacian Operator
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()






```

## OUTPUT:
### original image
![image](https://github.com/user-attachments/assets/7deaa419-a38c-4253-a455-628dac194c7d)


### 1. Smoothing Filters


i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/e8a9ed82-bd84-40b3-be05-774c8a469a42)


ii) Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/85738455-8b76-4188-a4cc-8db7636cf77e)


iii) Using Gaussian Filter
![image](https://github.com/user-attachments/assets/8c4e7e10-0923-4f82-bffe-cc2bc7f4be1e)


iv) Using Median Filter
![image](https://github.com/user-attachments/assets/f9c6b163-7ba5-4f0d-8ba0-377f30b8233f)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/8efc6aa2-4086-4245-b12a-16f7ef8c84df)


ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/7ce0bb20-dfad-4119-9d92-9ca9b28d812c)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
