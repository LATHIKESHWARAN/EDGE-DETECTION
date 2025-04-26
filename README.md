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
### Original Image
```
#Developed by : Lathikeshwaran J
#Register No: 212222230072
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('bird.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')




```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
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
![image](https://github.com/user-attachments/assets/32d905ea-42f7-4dfb-bc68-ca38809cad7d)



### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/a800ecbd-757a-4365-9fa0-9f38d6ccbd32)



### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/567ca31e-6b53-4c28-ae49-9dc99f7b38d9)


### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/870a4bab-500b-43c7-9d77-da6a991c0a8d)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
