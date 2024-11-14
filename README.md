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
```
Name: P Balasudhan
Register Number: 212222240017
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('peakpx.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)

# Display results using Matplotlib
plt.figure(figsize=(12, 12))

# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()

```
## Output:
### Original Image:
![Screenshot 2024-11-14 155957](https://github.com/user-attachments/assets/6334c263-7ae6-4483-a681-53cdb3db2527)
```
# Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```

## Output:
#### Original Image:
![Screenshot 2024-11-14 160006](https://github.com/user-attachments/assets/5646b3bc-77b3-483d-8b0d-3b30c83e1ea7)
```
# Display Original Image
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()

```

## Output:
### SOBEL EDGE DETECTION
![Screenshot 2024-11-14 160013](https://github.com/user-attachments/assets/fca8350f-b92f-46e3-9c47-8da901427232)

```
# Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()

```
## Output:
### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-11-14 160030](https://github.com/user-attachments/assets/1b70fc2d-dac4-4693-84e5-eb8bbe7b1707)

```
# Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
## Output:
### CANNY EDGE DETECTOR
![Screenshot 2024-11-14 160048](https://github.com/user-attachments/assets/98b55298-584b-4cc9-b79d-b73391546b97)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
