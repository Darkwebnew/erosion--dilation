# EX-09 Implementation-of-Erosion-and-Dilation
## Date: 25-04-2024
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

Step1:Import the necessary pacakages

Step2:Create the text using cv2.putText

Step3:Create the structuring element

Step4:Erode the Image

Step5:Dilate the Image

## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Good',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image

![image](https://github.com/Darkwebnew/erosion--dilation/assets/143114486/b2c504d3-8baf-4510-9138-d5bf2152b7a6)

### Display the Eroded Image

![image](https://github.com/Darkwebnew/erosion--dilation/assets/143114486/1ddfef41-01f3-4cb7-b7a0-cbda5bf7ee0a)

### Display the Dilated Image

![image](https://github.com/Darkwebnew/erosion--dilation/assets/143114486/5d7b610c-c1e2-415b-9db4-85b3270d8479)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
