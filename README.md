# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```

NAME:PREETHI A K
REGISTER NUMBER:212223230156

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="371" height="498" alt="image" src="https://github.com/user-attachments/assets/5ad6cdf9-593f-467f-bd5b-e25446ca709c" />

### SOBEL EDGE DETECTOR
<img width="359" height="494" alt="image" src="https://github.com/user-attachments/assets/513a7312-5520-4024-ad80-0730feeb47f0" />

### LAPLACIAN EDGE DETECTOR
<img width="367" height="496" alt="image" src="https://github.com/user-attachments/assets/3a3edd3a-ce0d-4194-96d5-2bed885a364a" />

### CANNY EDGE DETECTOR
<img width="381" height="514" alt="image" src="https://github.com/user-attachments/assets/23ec3c35-f2a0-41b7-af8f-fbad93b4b094" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
