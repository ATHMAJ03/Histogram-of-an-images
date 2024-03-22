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

```python
Developed By: ATHMAJ VENUGOPAL
Register Number: 212222240014
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("benzz.png")
color_image = cv2.imread("bmw.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("benzz.png")
Color_image = cv2.imread("bmw.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("benzz.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
![aa](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/0635eefb-b8e2-4e01-afd9-e9101a29999b)

![ab](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/515f7be4-77dc-4160-8ed1-410cd1944a5b)


### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -
![ac](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/341fb1b0-e9f9-4fb8-9235-87deb5fc1cae)

#### Color Image -
![ad](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/12bf4093-fc00-4af1-acc0-20af4e17503a)

### Histogram Equalization of Grayscale Image :
![ae](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/0f60fcf1-5a8d-4b48-bc52-f60156215b4e)

![af](https://github.com/ATHMAJ03/Histogram-of-an-images/assets/118753139/2588ebc9-ebe6-4fcd-8826-70481550e3b7)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
