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

#  Developed By: SRI SAI PRIYA.S
# Register Number: 212222240103

# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\grey.jpg')
color_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg',-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image
```
import numpy as np
import cv2
Gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\grey.jpg')
Color_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg')
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
```
# Histogram of Color image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg',0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<br>
<br>
<Br>
<br>
<br>
<Br>


## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/33bf6b3c-eb88-4c1b-85c9-a4059f21e3aa)

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/f1651535-6bf1-422b-b47c-ed1c12891a49)



### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/732a184d-4251-42cd-a561-1ed66b4c1aac)

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/0916e455-ea20-472c-bedd-9209dc5fbe92)

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/83540243-c2be-40af-bdff-db867f636cf4)

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/ffda9763-4d24-4f7c-9b2f-19d2a1a57be8)

### Histogram Equalization of Grayscale Image.

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/28510cd2-c356-4f69-81eb-1f320a267e22)

![image](https://github.com/SriSaiPriyaSenthilvel/Histogram-of-an-images/assets/119475702/92c52785-4aad-434c-8df8-c831437996bc)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
