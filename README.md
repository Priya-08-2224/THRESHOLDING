# THRESHOLDING

## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

## NAME : PRIYADHARSHINI J
## REG NO : 212224230210

## Load the necessary packages
```py
import cv2
import matplotlib.pyplot as plt

```

## Read the Image and convert to grayscale
```py
image=cv2.imread('pic.jpeg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
## Original Image
```py
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Use Global thresholding to segment the image
```py
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```

## Use Adaptive thresholding to segment the image
```py
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```

## Use Otsu's method to segment the image
```py
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```
## Global Thresholding
```py
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```

## Adaptive Thresholding
```py
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
## Otsu's Method
```py
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
## Show the plot
```py
plt.tight_layout()
plt.show()
```


## Output

### Original Image
<img width="1126" height="683" alt="image" src="https://github.com/user-attachments/assets/d0ad58e1-fd6f-4c5c-826c-2bb1ae05e026" />


### Global Thresholding
<img width="374" height="292" alt="image" src="https://github.com/user-attachments/assets/5a1f748b-cbc7-42c9-8a31-f5614e4c5a16" />

### Adaptive Thresholding
<img width="442" height="286" alt="image" src="https://github.com/user-attachments/assets/53692f4f-4fcd-4d6b-9db9-7c988d709339" />

### Optimum Global Thesholding using Otsu's Method
<img width="484" height="300" alt="image" src="https://github.com/user-attachments/assets/f132292e-3076-49a1-b696-81730614746a" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
