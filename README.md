# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it
### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image

### Name: PRAVEEN BV
### Register Number: 212222100036


 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt

#to read the color image
input_image_path='aakash.jpg'
color_image=cv2.imread(input_image_path)

#convert the color image to grayscale
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)

#perform edge detection using Canny
edges=cv2.Canny(gray_image,100,200)

#define the kernel size for erosion and dilation
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)

#perform erosion
erosion=cv2.erode(edges,kernel,iterations=1)

#perform dilation
dilation=cv2.dilate(edges,kernel,iterations=1)

#display all images
plt.figure(figsize=(15,10))

plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')

plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('Black and White Image')
plt.axis('on')

plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')

plt.subplot(2,3,4)
plt.imshow(erosion,cmap='gray')
plt.title('Erosion')
plt.axis('on')

plt.subplot(2,3,5)
plt.imshow(dilation,cmap='gray')
plt.title('Dilation')
plt.axis('on')

plt.show()
```
## Output:

### Display the input Image
![image](https://github.com/Praveen22042005/erosion-dilation/assets/112475766/45446c69-1081-4a64-9e04-0d103c5c6ac4)


### Display the Eroded Image
![image](https://github.com/Praveen22042005/erosion-dilation/assets/112475766/b7d56687-3792-4c3e-8181-c3f098be5837)

### Display the Dilated Image
![image](https://github.com/Praveen22042005/erosion-dilation/assets/112475766/03fec014-a4d8-4f76-aa39-4db5673790df)

### Full output
![image](https://github.com/Praveen22042005/erosion-dilation/assets/112475766/ee19068e-fdf3-47fb-8d0e-87bf6f74d939)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
