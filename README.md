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

## Code:

(i) Display the original image
```
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("rose.jpg")  # Replace with your image path
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
<img width="336" height="467" alt="image" src="https://github.com/user-attachments/assets/11534293-3af6-4e8a-ab81-ab6e7f7d9b4e" />


### SOBEL EDGE DETECTOR
<img width="303" height="469" alt="image" src="https://github.com/user-attachments/assets/9a779675-1a28-41b4-a5f9-3f5bcb2f8d91" />


### LAPLACIAN EDGE DETECTOR
<img width="335" height="471" alt="image" src="https://github.com/user-attachments/assets/7caeb932-c5e8-4590-83db-d913919f7002" />


### CANNY EDGE DETECTOR
<img width="334" height="470" alt="image" src="https://github.com/user-attachments/assets/c1dab02d-2b57-4aba-aa58-af2daea5b530" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
