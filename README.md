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

### Program : 

## Name: MUKESH KUMAR S
## register number: 212223230099

(i) Display the original image
```
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("Fish.jpg")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display Original Image
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()
```
(ii) Apply Sobel Edge Detection
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
# Display Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```
(iii) Apply Laplacian Edge Detection
```
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
# Display Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
```
(iv) Apply Canny Edge Detection
```
canny_edges = cv2.Canny(gray_image, 50, 150)
# Display Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```

## Output:
### ORIGINAL IMAGE

<img width="629" height="441" alt="image" src="https://github.com/user-attachments/assets/e018abea-116d-4d5b-9657-15feb67b4e32" />

### SOBEL EDGE DETECTOR

<img width="619" height="454" alt="image" src="https://github.com/user-attachments/assets/85b41c3f-32e3-451d-b6e1-2c003d5ea1e6" />

### LAPLACIAN EDGE DETECTOR

<img width="580" height="459" alt="image" src="https://github.com/user-attachments/assets/717d6d1b-99e2-4f9b-8013-83c606725bb1" />

### CANNY EDGE DETECTOR

<img width="587" height="451" alt="image" src="https://github.com/user-attachments/assets/9535ed8f-cbd6-4a25-bdc5-70d1c62e3c80" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
