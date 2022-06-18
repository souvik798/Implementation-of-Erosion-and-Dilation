# Implementation-of-Erosion-and-Dilation
## Aim:
To implement Erosion and Dilation using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step 1:
Import the necessary packages.
### Step 2:
Create the text image.
### Step 3:
Create the structuring image for dilation/erosion.
### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step 5:
Display the images.
 
## Program:
~~~
Developed by : Souvik Kundu 
Register Number : 212221230105
~~~
## Import the necessary packages:
~~~
import numpy as np 
import cv2
import matplotlib.pyplot as plt
~~~
## Create the Text using cv2.putText:
~~~
img1=np.zeros((100,500),dtype= 'uint8') 
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Souvik Kundu',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title("Original Image")
plt.axis('off')
~~~
## Create the structuring element:
~~~
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
~~~
## Erode the image:
~~~
image_erode = cv2.erode(img1,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,cmap='gray')
plt.axis('off')
~~~
## Dilate the image:
~~~
image_dilate = cv2.dilate(img1,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,cmap='gray')
plt.axis('off')
~~~
## Output:

### Display the input Image:

![output](1.png)

### Display the Eroded Image:

![output](2.png)

### Display the Dilated Image:

![output](3.png)

## Result:

Thus, the generated text image is eroded and dilated using python and OpenCV.