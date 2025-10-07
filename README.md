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

## Name: T.Roshini
## register number: 212223230175

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
<img width="336" height="467" alt="Screenshot 2025-10-07 153808" src="https://github.com/user-attachments/assets/e44e22d9-7e82-4857-a32b-b8430cadee2c" />


### SOBEL EDGE DETECTOR
<img width="303" height="469" alt="Screenshot 2025-10-07 153700" src="https://github.com/user-attachments/assets/3f24faa2-9a78-4b6e-8712-4d6c9195d244" />

### LAPLACIAN EDGE DETECTOR
<img width="335" height="471" alt="Screenshot 2025-10-07 153848" src="https://github.com/user-attachments/assets/46657d8b-e9b8-4cc8-8c90-6e30293cfe88" />

### CANNY EDGE DETECTOR
<img width="334" height="470" alt="Screenshot 2025-10-07 153915" src="https://github.com/user-attachments/assets/69b768f3-89d6-41fb-a27e-7173d31f4b73" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
