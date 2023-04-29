# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode and Dilate the image.

### Step5:
End Program.

 
## Program:

### Developed By : SAKTHISWAR S
### Ref No : 212222230127

``` Python
# Import the necessary packages

import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText

image1 = np.zeros((100,400), dtype = 'uint8')
image1 = cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image1,'Sakthi',(9,70), font, 2, (0,0,255),5,cv2.LINE_AA)

plt.figure()
plt.imshow(image1)
plt.title("original image")
plt.show()

# Create the structuring element

kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image_erode = cv2.erode(image1,kernel1)
image_dilation = cv2.dilate(image1, kernel1)



# Erode the image

plt.figure()
plt.imshow(image_erode)
plt.title("erosion")
plt.axis("off")
plt.show()


# Dilate the image

plt.figure()
plt.imshow(image_dilation)
plt.title("dilation")
plt.axis("off")
plt.show()


```
## Output:

### Display the input Image
![model](out1.png)

### Display the Eroded Image
![model](out2.png)

### Display the Dilated Image
![model](out3.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.