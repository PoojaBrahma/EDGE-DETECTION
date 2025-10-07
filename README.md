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

DEVELOPED BY : POOJA P

REGISTER NUMBER : 212224230195
``` py
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="246" height="403" alt="image" src="https://github.com/user-attachments/assets/41d51879-5440-4d33-acee-38a54dcf12ab" />

### SOBEL EDGE DETECTOR
``` py
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="240" height="403" alt="image" src="https://github.com/user-attachments/assets/34e182fa-6341-4a39-b3b4-b09ec33e7303" />

### LAPLACIAN EDGE DETECTOR
``` py
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="547" height="976" alt="image" src="https://github.com/user-attachments/assets/c9152e69-7be1-4683-ae36-16593f3fe75f" />

### CANNY EDGE DETECTOR
``` py
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="242" height="410" alt="image" src="https://github.com/user-attachments/assets/3dd0b45d-4b1e-431a-b862-82294b6aaafa" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
