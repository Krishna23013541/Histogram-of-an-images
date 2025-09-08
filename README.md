# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: ROGITH. K
# Register Number: 212223110042
```



### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread('image.png')
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Output:
<img width="593" height="509" alt="image" src="https://github.com/user-attachments/assets/a0150bd3-51d1-4da6-8761-8ab6cf2c3db8" />


### Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="811" height="536" alt="image" src="https://github.com/user-attachments/assets/bfab9fd3-b3e8-4470-b09b-d7779b4b3967" />


### Histogram Equalization of Grayscale Image.
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
## Output:

<img width="608" height="511" alt="image" src="https://github.com/user-attachments/assets/d3ca5b88-667f-4995-8fe5-7cdeae1d692f" />

## Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="756" height="553" alt="image" src="https://github.com/user-attachments/assets/e26e93cb-70de-48bb-bd5b-1f7beb8feb38" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
