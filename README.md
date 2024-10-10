# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Load the input image using cv2.imread().

### Step2:
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().

### Step3:
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.

### Step4:
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.

### Step5:
Use plt.subplot() to show the original, opening, and closing images side by side.

## Program:

```
Developed By : Iswarya P
Register no : 212223230082
```

### Import the necessary packages
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
```
### Load the image using cv2.imread()
```
image = cv2.imread("fly.jpeg")  
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Output
![image](https://github.com/user-attachments/assets/7a66551f-6ae6-47fd-a01d-a98e99529561)

### Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

### Use Opening operation
```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
### Output
![image](https://github.com/user-attachments/assets/e2b32d96-1b35-4ddb-aaca-c9b94a0e5e5a)

### Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
### Output
![image](https://github.com/user-attachments/assets/a182a9fe-9641-4a8e-a6eb-c8dfcfae6582)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
